<script>
  import "../app.css";
  import Footer from "../components/Footer.svelte";
  import Header from "../components/Header.svelte";
  import Skills from "../components/Skills.svelte";

  let y;
  let innerHeight = 0;
  let innerWidth = 0;

  function goTop() {
    document.body.scrollIntoView();
  }
</script>

<div
  class="relative flex flex-col max-w-[1400px] mx-auto w-full text-sm sm:text-base min-h-screen"
>
  <div
    class={"fixed bottom-0 right-0 duration-200 flex p-10 z-[10] " +
      (y > 0
        ? "opacity-full pointer-events-auto"
        : "opacity-none pointer-events-none")}
  >
    <button
      on:click={goTop}
      class="ml-auto rounded-full bg-violet-400 px-3 sm:px-4 hover:bg-slate-800 "
    >
      <i class="fa-solid fa-arrow-up grid place-items-center aspect-square" />
    </button>
  </div>

  <Header {y}/>
  <slot />
  <Skills/>
  <Footer />
</div>

<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />
