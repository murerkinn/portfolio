<template>
  <section id="projects">
    <Project
      v-for="(project, index) in projects"
      :key="index"
      :title="project.title"
      :imgPath="project.imgPath"
      :skills="project.skills"
      :overview="project.overview"
      :link="project.link"
    />
  </section>
</template>

<script>
import Project from "@/components/Project";

const projects = [
  {
    title: "Frontend Mentor Challenges",
    imgPath: "frontend-mentor.png",
    skills: [
      "HTML & SCSS",
      "Javascript",
      "Responsive Design"
    ],
    overview: "A library of my solutions for coding challenges found at frontendmentor.io",
    link: "/frontend-mentor",
    isRoute: true
  },
  {
    title: "Vue Covid Tracker",
    imgPath: "vue-covid-tracker.png",
    skills: [
      "Vue.js",
      "Javascript",
      "API",
      "Vuetify"
    ],
    overview: "Advanced Covid tracker app made with Vue.js. Users are able to see coronavirus cases all around the world.",
    link: "https://vue-covid-tracker.vercel.app/",
    isRoute: false
  },
  {
    title: "Vue Hangman",
    imgPath: "vue-hangman.png",
    skills: [
      "Vue.js",
      "Javascript",
      "HTML & CSS"
    ],
    overview: "Simple Hangman game made with Vue.js.",
    link: "https://vue-hangman.murerkinn.vercel.app/",
    isRoute: false
  }
]

export default {
  components: {
    Project
  },
  data: () => ({
    projects
  })
}
</script>

<style lang="scss" scoped>
  #projects {
  padding: 1em 5em;
  text-align: center;
}
</style>