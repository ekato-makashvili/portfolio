<template>
  <section
    class="relative w-full min-h-screen flex flex-col items-center justify-center bg-gradient-to-b from-gray-900 via-gray-800 to-gray-700 text-white px-6 overflow-x-hidden"
  >
    <!-- Name & Skills -->
    <div class="text-center space-y-6 relative z-10">
      <h1 class="text-4xl md:text-6xl font-extrabold tracking-tight">
        Ekaterine Makashvili
      </h1>

      <div class="flex flex-wrap justify-center gap-3 mt-6">
        <span
          v-for="(skill, index) in skills"
          :key="index"
          class="bg-gray-700/50 backdrop-blur-sm px-3 py-1 rounded-full text-sm md:text-base hover:bg-gray-600/60 transition transform hover:scale-105 cursor-pointer"
        >
          {{ skill }}
        </span>
      </div>

      <p class="text-md md:text-lg text-gray-300 mt-8 font-medium">
        Some of my recent projects
      </p>
    </div>

    <!-- Projects Grid -->
    <div
      class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-3 gap-5 mt-10 relative z-10"
    >
      <a
        v-for="(proj, index) in projects"
        :key="index"
        :href="proj.link"
        target="_blank"
        class="relative w-50 h-50 rounded-lg overflow-hidden shadow-md hover:shadow-lg transition-transform transform hover:scale-105 bg-black"
      >
        <img
          :src="proj.img"
          :alt="proj.title"
          class="w-full h-full object-cover rounded-lg transition duration-300 hover:brightness-90"
        />
        <div
          class="absolute bottom-0 left-0 w-full p-2 bg-gradient-to-t from-black/70 via-transparent to-transparent"
        >
          <h2 class="text-sm md:text-base font-semibold text-white">
            {{ proj.title }}
          </h2>
        </div>
      </a>
    </div>
  </section>
</template>

<script>
export default {
  name: "PortfolioSection",
  data() {
    return {
      projects: [
        {
          title: "Project 1",
          link: "https://yoga-game.netlify.app/",
          img: "https://res.cloudinary.com/dmr48sbbr/image/upload/v1763982959/lotus_rl8qxd.gif",
        },
        {
          title: "Project 2",
          link: "https://3d-galaxy-solar-system.netlify.app/",
          img: "https://res.cloudinary.com/dmr48sbbr/image/upload/v1763874767/solar_system_xw0vqh.gif",
        },
        {
          title: "Project 3",
          link: "https://zvirti-jewelry-store.netlify.app/",
          img: "project2.png",
        },
      ],
      skills: [
        "JavaScript",
        "Vue.js",
        "React.js",
        "Tailwind CSS",
        "Node.js",
        "Laravel",
        "MySQL/PostgreSQL",
      ],
    };
  },
};
</script>

<style scoped>
a img {
  transition: all 0.3s ease;
}
</style>
