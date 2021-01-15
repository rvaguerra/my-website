<template>
  <footer class="bg-gray-800">
    <div class="container mx-auto py-12">
      <div class="py-12 flex space-x-16">
        <div class="flex-1">
          <p class="footer-category">Contact</p>

          <ul class="space-y-6">
            <li v-for="link in links" :key="link.text">
              <a :href="link.url" class="footer-link">
                <i :class="link.icon" class="w-4 mr-4 text-center"></i>

                <span>{{ link.text }}</span></a
              >
            </li>
          </ul>
        </div>

        <nav class="flex-1">
          <p class="footer-category">Navigate</p>

          <ul class="space-y-6">
            <li class="footer-link"><a href="#hello">Hello</a></li>
            <li class="footer-link"><a href="#skills">Skills</a></li>
            <li class="footer-link"><a href="#my-work">My Work</a></li>
            <li class="footer-link">
              <a href="#testimonials">Testimonials</a>
            </li>
          </ul>
        </nav>
      </div>

      <div class="pt-12 pb-4 capitalized text-center text-gray-600">
        © 2021 Rodrigo Viégas Alves Guerra. All Rights Reserved.
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      links: [
        {
          text: "LinkedIn",
          url: "#",
          icon: "fab fa-linkedin",
        },
        {
          text: "GitHub",
          url: "#",
          icon: "fab fa-github",
        },
        {
          text: "My Email",
          url: "#",
          icon: "far fa-envelope",
        },
        {
          text: "CV/Resume",
          url: "#",
          icon: "far fa-file-alt",
        },
      ],
    };
  },
};
</script>

<style lang="postcss" scoped>
.footer-category {
  @apply pb-3 mb-6 text-gray-300 border-b border-gray-600;
}

.footer-link {
  @apply text-gray-400 hover:text-gray-100;
}
</style>