<template>
  <div class="project">
    <!-- <nuxt-link v-if="isRoute" :to="link">
      <img :src="`img/projects/${imgPath}`" alt="Project Thumbnail">
    </nuxt-link>
    <a v-else :href="link" target="_blank">
      <img :src="`img/projects/${imgPath}`" alt="Project Thumbnail">
    </a> -->
    <img :src="`img/projects/${imgPath}`" alt="Project Thumbnail">
    <div class="project-body">
      <h3 class="project-title">{{ title }}</h3>
      <div class="project-info">
        <div class="skills">
          <h4 class="project-subtitle">Skills</h4>
          <ul>
            <li class="skill-item" v-for="(skill, index) in skills" :key="index">{{ skill }}</li>
          </ul>
        </div>
        <div class="overview">
          <h4 class="project-subtitle">Overview</h4>
          <p class="overview-content">{{ overview }}</p>
        </div>
      </div>
    </div>
    <nuxt-link v-if="isRoute" :to="link" class="btn">View Projects</nuxt-link>
    <a v-else :href="link" class="btn">View Project</a>
  </div>
</template>

<script>
export default {
  name: "Project",
  props: {
    title: {
      type: String,
      required: true
    },
    imgPath: {
      type: String,
      required: true
    },
    skills: {
      type: Array,
      required: true
    },
    overview: {
      type: String,
      required: true
    },
    link: {
      type: String,
      required: true
    },
    isRoute: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style lang="scss" scoped>
.project {
  max-width: 1000px;
  margin: auto;

  &:not(:first-child) {
    margin-top: 5em;
  }
}

.project-body {
  padding: 2em 5em;
  text-align: left;
  font-family: 'Josefin Sans', sans-serif;
}

.project-title,
.project-subtitle {
  font-family: 'Josefin Sans', sans-serif;
  text-transform: uppercase;
  margin-bottom: 1em;
  font-weight: 400;
}

.project-title {
  line-height: 42px;
  font-size: 28px;
  letter-spacing: 1.68px;
  font-weight: 700;
}

.project-info {
  display: flex;

  .skills {
    flex: 1;

    .skill-item {
      font-weight: 300;
      line-height: 25.2px;
    }
  }

  .overview {
    flex: 2;
    font-weight: 300;
    line-height: 20px;
  }

  @media only screen and (max-width: 740px) {
    flex-direction: column;

    .overview {
      margin-top: 2em;
    }
  }
}
</style>
