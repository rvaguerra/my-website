<template>
  <h2 class="capitalize font-medium text-3xl">{{ title }}</h2>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: "Section Title",
    },
  },
};
</script>