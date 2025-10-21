<template>
  <div class="w-full max-w-2xl text-center space-y-4">
    <div
      class="flex md:flex-nowrap flex-wrap justify-center items-center gap-8 text-gray-300 md:text-xl text-center"
    >
      <a
        :href="linkedin"
        target="_blank"
        class="hover:text-white transition flex items-center gap-2"
      >
        <img src="/icons/linkedin.png" alt="LinkedIn" class="w-6 h-6" />
        LinkedIn
      </a>

      <a
        :href="github"
        target="_blank"
        class="hover:text-white transition flex items-center gap-2"
      >
        <img src="/icons/github.png" alt="GitHub" class="w-6 h-6" />
        GitHub
      </a>

      <a
        :href="'mailto:' + email"
        class="hover:text-white transition flex items-center gap-2"
      >
        <img src="/icons/mail.png" alt="Email" class="w-6 h-6" />
        {{ email }}
      </a>

      <a
        :href="'tel:' + phone"
        class="hover:text-white transition flex items-center gap-2"
      >
        <img src="/icons/phone.png" alt="Phone" class="w-6 h-6" />
        {{ phone }}
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "Contact",
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
