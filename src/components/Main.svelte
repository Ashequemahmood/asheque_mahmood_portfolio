<script>
  import Step from "./Step.svelte";

  let steps = [
    {
      name: "E-Commerce Web Application",
      icon: "fa-solid fa-cart-shopping",
      description:
        "Built a fully functional e-commerce web application using React for the front-end and Node.js/Express.js for the back-end.",
    },
    {
      name: "Quiz Service Platform",
      icon: "fa-solid fa-list-check",
      description:
        "Created a quiz service platform with svelte to  assist learners in testing and enhancing their knowledge across a variety of subjects, offering a well-structured and enjoyable approach to the learning journey.",
    },
    {
      name: "Pokédex",
      icon: "fa-solid fa-diagram-project",
      description:
        "Augment your datasets with our filters and dataset manipulations to ensure your models are trained on the highest quality datasets (coming soon).",
    },
  ];

  let benefits = [
    {
      metric: "10x",
      name: "a self taught developer",
      description:
        "I taught myself to code using free online resources and absolutely fell in love with the creativity and problem solving that is involved in developing and engineering innovative new online experiences. Starting of with JavaScript, HTML & CSS and evolving my knowledge base to include JavaScript frameworks, backend programming, design, cloud services and much much more.",
    },
    {
      name: "a product design & UX finatic",
      description:
        "Carefully crafting and designing amazing user experiences allows me to express and experiment with every morsel of creativity I have. I love the challenge of learning new design concepts and enabling users with amazing online experiences.",
    },
    {
      name: "an excellent communicator",
      description:
        "Communication is key and it's a paramount value of mine. I believe in transparency and constructive communication above all else. This helps me develop deep relationships and ensures my effectiveness and productivity in any work space with any team.",
    },
  ];
</script>

<main class="flex flex-col flex-1 p-4">
  <section
    id="introPage"
    class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14 px-4"
  >
    <div
      class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-18"
    >
      <h1 class="font-semibold text-3xl sm:text-4xl lg:text-5xl">
        Hi! I'm <span class="text-violet-400">Asheque</span> Mahmood<br />Full
        Stack <span class="poppins text-violet-400">Developer</span>
      </h1>
      <p class="text-base sm:text-lg md:text-xl">
        My <span class="text-violet-400">favorite</span> tech includes JavaScript
        (React or SvelteKit), TailwindCSS, Node.js + Express.js, Deno + Hono, PostgreSQL
        + MongoDB or Firebase
      </p>
      <a
        href="#"
        target="_blank"
        class="blueShadow bg-white text-slate-950 py-3 px-6 rounded-full overflow-hidden poppins relative mx-auto lg:ml-0 text-base sm:text-lg md:text-xl"
      >
        <div
          class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
        ></div>
        <h4 class="relative z-9">Get in touch &rarr;</h4>
      </a>
    </div>

    <div class="relative shadow-2xl grid place-items-center">
      <img
        src={"images/fotor.jpg"}
        alt=""
        class="object-cover z-[2] max-h-[35vh] sm:max-h-[50vh] lg:max-h-[60vh] rounded-full"
      />
    </div>
  </section>

  <!-- projects -->
  <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-large sm:text-xl md:text-2xl">
        A few of my creative endeavors.
      </h6>
      <h3 class="font-semibold text-2xl sm:text-3xl md:text-4xl">
        Curious to <span class="poppins text-violet-400">see</span> my work?
      </h3>
    </div>
    <a
      href="#"
      target="_blank"
      class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200"
    >
      <i class="fa-regular fa-circle-play" />
      <p>Watch the video</p>
    </a>
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
      <Step step={steps[0]}>
        <p>
          Built a fully functional e-commerce web application using React for
          the front-end and Node.js/Express.js for the back-end.
        </p>
      </Step>
      <Step step={steps[1]}>
        <p>
          Created a quiz service platform with svelte to assist learners in
          testing and enhancing their knowledge across a variety of subjects,
          offering a well-structured and enjoyable approach to the learning
          journey.
        </p>
      </Step>
      <Step step={steps[2]}>
        <p>
          The Pokédex is a <strong class="text-violet-400"
            >SvelteKit & TailwindCSS</strong
          >
          web application, hosted on
          <strong class="text-violet-400">Netlify</strong>, that consumes and
          caches the
          <strong class="text-violet-400">Pokémon API</strong>
          to display all Pokémon information. Gotta catch them all!
        </p>
      </Step>
    </div>
  </section>
  <section
    id="about"
    class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
  >
    <!-- <div class="z-[-1] bg-violet-950 w-screen left-1/2 -translate-x-1/2 top-0 h-full absolute"> </div> -->
    <div
      class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
    >
      <h6 class="text-large sm:text-xl md:text-2xl">Want to know more?</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        A bit <span class="poppins text-violet-400">about</span> me.
      </h3>
    </div>
    <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
      I am . . .
    </p>
    <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
      {#each benefits as benefit, index}
        <!-- <div class="flex flex-col gap-2 mx-auto">
                    <div class="flex items-end gap-4">
                        <p
                            class="poppins text-6xl sm:text-7xl md:text-8xl text-slate-500 font-medium"
                        >
                            {benefit.metric}
                        </p>
                        <p
                            class="text-xl sm:text-2xl md:text-3xl capitalize pb-2"
                        >
                            {benefit.name}
                        </p>
                    </div>
                    <p class="text-center italic">- {benefit.description}</p>
                </div> -->
        <div class="flex gap-6 sm:gap-8">
          <p
            class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
          >
            0{index + 1}
          </p>
          <div class="flex flex-col gap-6 sm:gap-8">
            <h3 class="text-2xl sm:text-3xl md:text-5xl">
              {benefit.name}
            </h3>
            <p>{benefit.description}</p>
          </div>
        </div>
      {/each}
    </div>

    <div
      class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
    >
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        My <span class="poppins text-violet-400">skills</span>
      </h3>
    </div>
  </section>
</main>
