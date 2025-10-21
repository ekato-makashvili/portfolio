<template>
  <footer class="fixed bottom-0 left-0 w-full bg-gray-900/95 border-t border-gray-700 py-4 px-4 md:px-8 z-50">
    <div class="flex flex-col md:flex-row justify-center items-center gap-4 md:gap-8 text-gray-300 text-sm md:text-base">
      
      <a
        :href="linkedin"
        target="_blank"
        class="flex items-center gap-2 hover:text-white transition"
      >
        <img src="/icons/linkedin.png" alt="LinkedIn" class="w-5 h-5 md:w-6 md:h-6" />
        LinkedIn
      </a>

      <a
        :href="github"
        target="_blank"
        class="flex items-center gap-2 hover:text-white transition"
      >
        <img src="/icons/github.png" alt="GitHub" class="w-5 h-5 md:w-6 md:h-6" />
        GitHub
      </a>

      <a
        :href="'mailto:' + email"
        class="flex items-center gap-2 hover:text-white transition break-all"
      >
        <img src="/icons/mail.png" alt="Email" class="w-5 h-5 md:w-6 md:h-6" />
        {{ email }}
      </a>

      <a
        :href="'tel:' + phone"
        class="flex items-center gap-2 hover:text-white transition"
      >
        <img src="/icons/phone.png" alt="Phone" class="w-5 h-5 md:w-6 md:h-6" />
        {{ phone }}
      </a>

    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      linkedin: "https://www.linkedin.com/in/ekaterine-makashvili-09b936194/",
      github: "https://github.com/ekato-makashvili",
      email: "ekaterinemakashvili@gmail.com",
      phone: "+995595291775",
    };
  },
};
</script>

<style>
/* Optional: fix icon alignment on small screens */
footer img {
  display: inline-block;
  vertical-align: middle;
}
</style>
