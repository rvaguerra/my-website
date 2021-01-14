<template>
  <section>
    <SectionContainer title="My Skills">
      <SectionParagraph>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat, dolorum
        sunt sint quibusdam maiores non pariatur assumenda quo molestiae velit
        minima eveniet praesentium et reiciendis suscipit. Ut omnis commodi
        laborum.
      </SectionParagraph>

      <SkillList :skills="skills"></SkillList>
    </SectionContainer>
  </section>
</template>

<script>
import SectionContainer from "./ui/Section/Container";
import SectionParagraph from "./ui/Section/Paragraph";
import SkillList from "./ui/Skills/List";

export default {
  components: {
    SectionContainer,
    SectionParagraph,
    SkillList,
  },

  data() {
    return {
      skills: [
        {
          label: "Node.js",
          icon: "fab fa-node-js",
          color: "green-600",
        },
        {
          label: "Vue.js",
          icon: "fab fa-vuejs",
          color: "green-500",
        },
        {
          label: "JavaScript",
          icon: "fab fa-js-square",
          color: "yellow-400",
        },
        {
          label: "PHP",
          icon: "fab fa-php",
          color: "indigo-500",
        },
        {
          label: "Laravel",
          icon: "fab fa-laravel",
          color: "red-500",
        },
        {
          label: "WordPress",
          icon: "fab fa-wordpress",
          color: "blue-900",
        },
        {
          label: "MySQL | SQL",
          icon: "fas fa-database",
          color: "blue-500",
        },
        {
          label: "HTML",
          icon: "fab fa-html5",
          color: "blue-500",
        },
        {
          label: "CSS",
          icon: "fab fa-css3-alt",
          color: "yellow-600",
        },
        {
          label: "Bootstrap",
          icon: "fab fa-bootstrap",
          color: "indigo-900",
        },
        {
          label: "Python",
          icon: "fab fa-python",
          color: "blue-500",
        },
        {
          label: "Git",
          icon: "fab fa-git",
          color: "red-500",
        },
        {
          label: "Web Hosting",
          icon: "fas fa-cloud",
          color: "blue-400",
        },
        {
          label: "Discord Bots",
          icon: "fab fa-discord",
          color: "indigo-500",
        },
        {
          label: "Others...",
          icon: "fas fa-ellipsis-h",
          color: "gray-400",
        },
      ],
    };
  },
};
</script>