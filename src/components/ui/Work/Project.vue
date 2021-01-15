<template>
  <article class="flex projects-wrapper">
    <div
      v-if="hasCover"
      class="flex-1 bg-cover bg-center"
      :style="`background-image: url(${cover})`"
    ></div>

    <div class="flex-1">
      <div class="p-12 space-y-6">
        <h2 class="text-xl uppercase text-gray-600">
          <slot name="title"></slot>
        </h2>

        <p class="text-gray-500">
          <slot name="content"></slot>
        </p>

        <div class="flex flex-wrap" v-if="hasSkills">
          <ProjectSkill v-for="skill in skills" :key="skill">
            {{ skill }}
          </ProjectSkill>
        </div>
      </div>
    </div>
  </article>
</template>

<script>
import ProjectSkill from "./Skill";

export default {
  components: {
    ProjectSkill,
  },

  props: {
    cover: {
      type: String,
      default: "",
    },

    skills: {
      type: Array,
      default: () => [],
    },
  },

  computed: {
    hasCover() {
      return this.cover.length > 0;
    },

    hasSkills() {
      return this.skills.length > 0;
    },
  },
};
</script>