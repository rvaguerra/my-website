<template>
  <section>
    <SectionContainer title="Testimonials">
      <SectionParagraph>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat, dolorum
        sunt sint quibusdam maiores non pariatur assumenda quo molestiae velit
        minima eveniet praesentium et reiciendis suscipit. Ut omnis commodi
        laborum.
      </SectionParagraph>

      <div class="flex items-stretch space-x-12">
        <div
          v-for="testimonial in testimonials"
          :key="testimonial.name"
          class="flex flex-1 flex-col justify-between border border-gray-200 shadow-lg rounded-lg"
        >
          <p class="flex flex-grow items-center p-12">
            {{ testimonial.content }}
          </p>

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
  </section>
</template>

<script>
import SectionParagraph from "./ui/Section/Paragraph";
import SectionContainer from "./ui/Section/Container";

export default {
  components: {
    SectionParagraph,
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