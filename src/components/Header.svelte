<script>
  export let y;

  let tabs = [
    { name: "Projects", link: "#projects" },
    { name: "About me", link: "#about" },
  ];
</script>

<header
  class={"sticky top-0 z-[10] flex justify-between items-center px-6 duration-200 border border-solid " +
    (y > 0
      ? "py-4 bg-slate-950 border-violet-950"
      : "py-6 bg-transparent border-transparent")}
>
  <h1 class="font-medium">
    <b class="font-bold poppins">Asheque</b> Mahmood
  </h1>
  <div class="sm:flex items-center gap-4 hidden">
    {#each tabs as tab}
      <a href={tab.link} class="duration-200 hover:text-violet-400">
        <p>{tab.name}</p>
      </a>
    {/each}
  </div>

  <a
    href="#"
    target="_blank"
    class="bg-white text-slate-950 py-2 px-5 rounded-full overflow-hidden relative"
  >
  <div>
    
  </div>
    <h4>Get in touch</h4>
  </a>
</header>
