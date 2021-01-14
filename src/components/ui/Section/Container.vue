<template>
  <article class="container mx-auto py-32">
    <SectionTitle :title="title"></SectionTitle>
    <SectionSubTitle :subTitle="subTitle"></SectionSubTitle>

    <div class="mt-8 tracking-wider leading-loose">
      <slot></slot>
    </div>
  </article>
</template>

<script>
import SectionTitle from "./Title";
import SectionSubTitle from "./SubTitle";

export default {
  components: {
    SectionTitle,
    SectionSubTitle,
  },
  props: {
    title: {
      type: String,
    },

    subTitle: {
      type: String,
    },
  },
};
</script>