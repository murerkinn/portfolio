<template>
  <div>
    <section id="intro">
      <h1 class="intro-title">
        Hi, I'm Erkin.<br><br>
        I’m a Full Stack Developer.
        Passionate about <span>software architecture</span>, <span>web application security</span> and <span>cloud computing</span>.
      </h1>
    </section>

    <section id="projects">
      <Project
        v-for="(project, index) in projects"
        :key="index"
        :title="project.title"
        :imgPath="project.imgPath"
        :skills="project.skills"
        :overview="project.overview"
        :link="project.link"
        :isRoute="project.isRoute"
      />
    </section>
  </div>
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
    title: "Nuxt Admin",
    imgPath: "nuxt-admin.png",
    skills: [
      "Nuxt.js",
      "Vue.js",
      "Node.js",
      "MongoDB"
    ],
    overview: "An open source Nuxt Admin panel that I'm still working on. It will be used as a template with wonderful features.",
    link: "https://github.com/murerkinn/nuxt-admin",
    isRoute: false
  },
  {
    title: "Vuoter",
    imgPath: "vuoter.png",
    skills: [
      "Vue.js",
      "Node.js",
      "MongoDB",
      "Socket.io"
    ],
    overview: "An open source voting app that I'm still working on. Users will be able to write down their ideas and vote other people's ideas.",
    link: "https://github.com/murerkinn/vuoter",
    isRoute: false
  },
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
/* [SECTION] Projects */
#projects {
  padding: 1em 5em;
  text-align: center;
}
</style>
