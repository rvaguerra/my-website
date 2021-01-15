<template>
  <SectionContainer class="pattern-background">
    <template v-slot:title>Testimonials</template>

    <div class="flex items-stretch space-x-12">
      <div
        v-for="testimonial in testimonials"
        :key="testimonial.name"
        class="flex flex-1 flex-col justify-between border border-gray-200 shadow-lg rounded-lg bg-white"
      >
        <div class="p-12 pb-20 flex flex-grow items-center">
          <p class="italic">
            <i class="fas fa-quote-left text-gray-300"></i>
            {{ testimonial.content }}
            <i class="fas fa-quote-right text-gray-300"></i>
          </p>
        </div>

        <div
          class="p-8 rounded-b-lg text-center"
          :class="`bg-${testimonial.color}`"
        >
          <img
            class="-mt-16 mb-4 mx-auto rounded-full w-16"
            src="https://media-exp1.licdn.com/dms/image/C4D03AQFBHMr-5FEASw/profile-displayphoto-shrink_400_400/0/1551119252073?e=1616025600&v=beta&t=wjhL5JPH8fUUG9-ISWjvze8ZfxVZdguKyW-7cEz9bjI"
            alt="avatar"
          />

          <p class="mb-2 text-gray-100 text-lg font-medium">
            {{ testimonial.name }}
          </p>

          <p class="text-gray-100 text-sm">
            {{ testimonial.jobTitle }} @ {{ testimonial.company }}
          </p>
        </div>
      </div>
    </div>
  </SectionContainer>
</template>

<script>
import SectionContainer from "./ui/Section/Container";

export default {
  components: {
    SectionContainer,
  },

  data() {
    return {
      testimonials: [
        {
          content:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Dolorem minus fugiat sapiente doloribus cum, quas, excepturi, voluptatem amet cumque quaerat minima quam repellendus.",
          avatar: "",
          name: "Full Name",
          jobTitle: "Job Title",
          company: "Company Name",
          color: "red-500",
        },

        {
          content:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Dolorem minus fugiat sapiente doloribus cum, quas, excepturi, voluptatem amet cumque quaerat minima quam repellendus. Quis sed molestiae animi architecto reiciendis ipsum?",
          avatar: "",
          name: "Full Name",
          jobTitle: "Job Title",
          company: "Company Name",
          color: "indigo-500",
        },

        {
          content:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Dolorem minus fugiat sapiente doloribus cum, quas, excepturi.",
          avatar: "",
          name: "Full Name",
          jobTitle: "Job Title",
          company: "Company Name",
          color: "green-500",
        },
      ],
    };
  },
};
</script>


<style lang="postcss" scoped>
.pattern-background {
  background-image: url("data:image/svg+xml,%3Csvg width='120' height='120' viewBox='0 0 120 120' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M9 0h2v20H9V0zm25.134.84l1.732 1-10 17.32-1.732-1 10-17.32zm-20 20l1.732 1-10 17.32-1.732-1 10-17.32zM58.16 4.134l1 1.732-17.32 10-1-1.732 17.32-10zm-40 40l1 1.732-17.32 10-1-1.732 17.32-10zM80 9v2H60V9h20zM20 69v2H0v-2h20zm79.32-55l-1 1.732-17.32-10L82 4l17.32 10zm-80 80l-1 1.732-17.32-10L2 84l17.32 10zm96.546-75.84l-1.732 1-10-17.32 1.732-1 10 17.32zm-100 100l-1.732 1-10-17.32 1.732-1 10 17.32zM38.16 24.134l1 1.732-17.32 10-1-1.732 17.32-10zM60 29v2H40v-2h20zm19.32 5l-1 1.732-17.32-10L62 24l17.32 10zm16.546 4.16l-1.732 1-10-17.32 1.732-1 10 17.32zM111 40h-2V20h2v20zm3.134.84l1.732 1-10 17.32-1.732-1 10-17.32zM40 49v2H20v-2h20zm19.32 5l-1 1.732-17.32-10L42 44l17.32 10zm16.546 4.16l-1.732 1-10-17.32 1.732-1 10 17.32zM91 60h-2V40h2v20zm3.134.84l1.732 1-10 17.32-1.732-1 10-17.32zm24.026 3.294l1 1.732-17.32 10-1-1.732 17.32-10zM39.32 74l-1 1.732-17.32-10L22 64l17.32 10zm16.546 4.16l-1.732 1-10-17.32 1.732-1 10 17.32zM71 80h-2V60h2v20zm3.134.84l1.732 1-10 17.32-1.732-1 10-17.32zm24.026 3.294l1 1.732-17.32 10-1-1.732 17.32-10zM120 89v2h-20v-2h20zm-84.134 9.16l-1.732 1-10-17.32 1.732-1 10 17.32zM51 100h-2V80h2v20zm3.134.84l1.732 1-10 17.32-1.732-1 10-17.32zm24.026 3.294l1 1.732-17.32 10-1-1.732 17.32-10zM100 109v2H80v-2h20zm19.32 5l-1 1.732-17.32-10 1-1.732 17.32 10zM31 120h-2v-20h2v20z' fill='%239C92AC' fill-opacity='0.07' fill-rule='evenodd'/%3E%3C/svg%3E");
}
</style>