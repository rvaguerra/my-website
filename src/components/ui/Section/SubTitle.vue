<template>
  <div v-if="subTitle" class="pb-8 flex justify-center text-center">
    <h2 class="w-2/3 capitalize text-3xl tracking-widest">
      {{ subTitle }}
    </h2>
  </div>
</template>

<script>
export default {
  props: {
    subTitle: {
      type: String,
      default: "",
    },
  },
};
</script>