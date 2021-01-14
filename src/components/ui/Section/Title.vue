<template>
  <div v-if="title" class="pb-8 flex justify-center text-center">
    <h2 class="capitalize font-medium text-5xl tracking-widest">
      {{ title }}
    </h2>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
    },
  },
};
</script>