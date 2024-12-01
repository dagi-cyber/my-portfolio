<script>
  import Step from "./Step.svelte";

  // Steps for the projects
  let Steps = [
    { name: "Alumni Management System", icon: "fa-solid fa-list-check" },
    { name: "Online Examination System", icon: "fa-solid fa-school" }
  ];

  // Benefits section
  let benefits = [
    { name: 'Good Problem Solving', description: 'I have developed a strong problem-solving skillset through various coding challenges and projects.' },
    { name: 'Excellent for Learning New Things', description: 'Every project teaches me something new, keeping me constantly engaged and improving.' }
  ];
</script>

<main class="flex flex-col flex-1 p-4">
  <!-- Intro Section -->
  <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
    <!-- Text and Intro Content -->
    <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Hi, I'm <span class="poppins text-violet-400">Dagmawi Temesgen</span><br />Full Stack 
        <span class="poppins text-violet-400">Developer</span>
      </h2>
      <p class="text-base sm:text-lg md:text-xl">
        I have <span class="text-violet-400">worked on </span>Html, Css, Php, Mysql, JavaScript, and some skills in React, Laravel, Java, C++, and more!
      </p>
    

    <!-- Contact Button -->
    <!-- svelte-ignore a11y_invalid_attribute -->
      <a
         class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-6 group rounded-full bg-white text-slate-950 cursor-pointer"
         href="#"
         target="_blank"
     >
      <!-- svelte-ignore element_invalid_self_closing_tag -->
        <div 
            class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200" 
        />
        <h4 class="relative z-10">Get In Touch &rarr;</h4>
      
    </a>

    <!-- Profile Image -->
    <div class="relative shadow-2xl grid place-items-center">
      <!-- svelte-ignore a11y_img_redundant_alt -->
      <img
        src={"images/messi-holding-barcelona-jersey-p6y6jbb21dpne97r.png"}
        alt="Profile image"
        class="object-cover z-[2] max-h-[70vh]"
      />
    </div>
  </section>

  <!-- Projects Section -->
  <section id="projects" class="py-20 lg:pt-32 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl">
        A few of my works.
      </h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        Want to <span class="poppins text-violet-400">see</span> my work?
      </h3>
    </div>

    <!-- Project Steps Grid -->
      <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
        <Step step={Steps[0]}>
          <p>Alumni Management System created with <strong class="text-violet-400">Html, Css, JavaScript, Php</strong>, MySQL that allows a user to login, manage events, appointments, and more.</p>
        </Step>
       <Step step={Steps[1]}>
        <p>Online Examination System created with <strong class="text-violet-400">Html, Css, JavaScript, Php</strong>, MySQL that allows a user to login, manage, and take exams.</p>
       </Step>
      </div>
  </section>

  <!-- About Section -->
  <section
    id="about"
    class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
  >
    <!-- Section Heading -->
    <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0
      before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute
      after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700">
      <h6 class="text-lg sm:text-xl md:text-2xl">Want To Know More</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        A bit <span class="poppins text-violet-400">about</span> me.
      </h3>
    </div>

    <!-- Empty Paragraph (can be filled with additional info about you) -->
    <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I graduated Computer Science from Ambo University 2024</p>

    <!-- Benefits List -->
    <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
      {#each benefits as benefit, index}
        <div class="flex gap-6 sm:gap-8">
          <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">0{index+1}</p>
          <div class="flex flex-col gap-6 sm:gap-8">
            <h3 class="text-2xl sm:text-3xl md:text-5xl">
              {benefit.name}
            </h3>
            <p>{benefit.description}</p>
          </div>
        </div>
      {/each}
    </div>
  </section>
</main>

<style>
  .poppins {
    font-family: 'Poppins', sans-serif;
  }
</style>

