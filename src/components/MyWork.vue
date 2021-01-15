<template>
  <SectionContainer>
    <template v-slot:title>My Work</template>

    <template v-slot:sub-title
      >Lorem ipsum dolor sit amet consectetur, adipisicing elit.
    </template>

    <div class="space-y-12">
      <Project
        v-for="project in projects"
        :key="project.title"
        :cover="project.cover"
        :skills="project.skills"
      >
        <template v-slot:title>
          {{ project.title }}
        </template>

        <template v-slot:content>
          {{ project.content }}
        </template>
      </Project>
    </div>
  </SectionContainer>
</template>

<script>
import SectionContainer from "./ui/Section/Container";
import Project from "./ui/Work/Project";

export default {
  components: {
    SectionContainer,
    Project,
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