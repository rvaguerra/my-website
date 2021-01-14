<template>
  <section>
    <SectionContainer title="My Work">
      <SectionParagraph
        >Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat,
        dolorum sunt sint quibusdam maiores non pariatur assumenda quo molestiae
        velit minima eveniet praesentium et reiciendis suscipit. Ut omnis
        commodi laborum.
      </SectionParagraph>

      <SectionParagraph class="space-y-12">
        <article
          v-for="project in projects"
          :key="project.title"
          class="flex projects-wrapper"
        >
          <div
            class="flex-1 bg-cover bg-center"
            :style="`background-image: url(${project.cover})`"
          ></div>

          <div class="flex-1">
            <div class="p-12 space-y-6">
              <h2 class="text-xl uppercase text-gray-600">
                {{ project.title }}
              </h2>

              <p class="text-gray-500">{{ project.content }}</p>

              <div class="flex flex-wrap">
                <span
                  v-for="skill in project.skills"
                  :key="skill"
                  class="my-1 mr-2 px-4 py-1 border text-xs"
                  >{{ skill }}</span
                >
              </div>
            </div>
          </div>
        </article>
      </SectionParagraph>
    </SectionContainer>
  </section>
</template>

<script>
import SectionContainer from "./ui/Section/Container";
import SectionParagraph from "./ui/Section/Paragraph";

export default {
  components: {
    SectionContainer,
    SectionParagraph,
  },

  data() {
    return {
      projects: [
        {
          title: "Project Name | Company",
          content:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Voluptatem vero sint porro non.",
          cover:
            "https://images.pexels.com/photos/1591447/pexels-photo-1591447.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500",
          skills: ["API", "Back-end", "Front-end", "Hosting"],
        },
        {
          title: "Project Name | Company",
          content:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Voluptatem vero sint porro non. Labore provident fugiat laborum facilis reprehenderit natus illo facere aperiam aliquid maxime neque dignissimos sed, ullam animi.",
          cover:
            "https://i.pinimg.com/originals/af/8d/63/af8d63a477078732b79ff9d9fc60873f.jpg",
          skills: [
            "API",
            "Back-end",
            "Front-end",
            "Hosting",
            "Back-end",
            "Front-end",
            "Hosting",
            "Back-end",
            "Front-end",
            "Hosting",
            "Back-end",
            "Front-end",
            "Hosting",
          ],
        },
        {
          title: "Project Name | Company",
          content:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Voluptatem vero sint porro non.",
          cover:
            "https://images.pexels.com/photos/1591447/pexels-photo-1591447.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500",
          skills: ["API", "Back-end", "Front-end", "Hosting"],
        },
      ],
    };
  },
};
</script>

<style lang="postcss" scoped>
.projects-wrapper:nth-child(even) {
  @apply flex-row-reverse;
}
</style>