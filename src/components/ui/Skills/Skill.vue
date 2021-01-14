<template>
  <i :class="[icon, `text-${color}`]" class="text-6xl text-gray-400"></i>

  <span class="text-sm text-gray-400">{{ label }}</span>
</template>

<script>
export default {
  props: {
    icon: {
      type: String,
    },

    color: {
      type: String,
    },

    label: {
      type: String,
    },
  },
};
</script>