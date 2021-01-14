<template>
  <NavigationBar></NavigationBar>

  <Hello></Hello>
  <MySkills></MySkills>
  <MyWork></MyWork>
  <Testimonials></Testimonials>

  <AppFooter></AppFooter>
</template>

<script>
import NavigationBar from "./components/NavigationBar";
import Hello from "./components/Hello";
import MySkills from "./components/MySkills";
import MyWork from "./components/MyWork";
import Testimonials from "./components/Testimonials";
import AppFooter from "./components/AppFooter";

export default {
  components: {
    NavigationBar,
    Hello,
    MySkills,
    MyWork,
    Testimonials,
    AppFooter,
  },
};
</script>