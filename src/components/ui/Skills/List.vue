<template>
  <div class="py-6 grid grid-cols-5 gap-16">
    <div
      class="flex flex-col text-center space-y-4"
      v-for="skill in skills"
      :key="skill.label"
    >
      <Skill
        :label="skill.label"
        :color="skill.color"
        :icon="skill.icon"
      ></Skill>
    </div>
  </div>
</template>

<script>
import Skill from "./Skill";

export default {
  components: {
    Skill,
  },

  props: {
    skills: {
      type: Object,
    },
  },
};
</script>