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
  class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-2 mt-6 relative z-10 max-w-4xl mx-auto"
>
  <a
    v-for="(proj, index) in projects"
    :key="index"
    :href="proj.link"
    target="_blank"
    rel="noopener noreferrer"
    class="group relative rounded-lg overflow-hidden shadow-md hover:shadow-lg transition-all duration-300 transform hover:scale-[1.03] bg-gray-900"
  >
    <!-- Project Image -->
    <div class="relative w-full aspect-square overflow-hidden">
      <img
        :src="proj.img"
        :alt="proj.title"
        class="w-full h-full object-cover transition duration-500 group-hover:scale-105"
      />
    </div>

    <!-- Project Info -->
    <div class="p-2">
      <h2 class="text-xs md:text-sm font-semibold text-white mb-1">
        {{ proj.title }}
      </h2>

      <p class="text-[11px] text-gray-400 leading-snug">
        {{ proj.description }}
      </p>
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
          title: "3D Galaxy",
          link: "https://3d-galaxy-solar-system.netlify.app/",
          img: "https://res.cloudinary.com/dmr48sbbr/image/upload/v1763874767/solar_system_xw0vqh.gif",
          description: "A 3D solar system simulation built with Three.js, allowing users to explore the planets.",
        },
                {
          title: "Yoga Quiz",
          link: "https://yoga-quiz.netlify.app/",
          img: "https://res.cloudinary.com/dmr48sbbr/image/upload/v1763982959/lotus_rl8qxd.gif",
          description: "An interactive yoga quiz to test your knowledge of various poses and techniques.",
        },
        {
          title: "Zvirti Jewelry",
          link: "https://zvirti.netlify.app/",
          img: "zvirti.gif",
          description: "A modern jewelry brand showcasing elegant pieces.",
        },
                        {
          title: "Outdoor Yoga",
          link: "https://yoga-nature.onrender.com/",
          img: "lotus.png",
          description: "Yoga classes in nature with online registration and payment.",
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
