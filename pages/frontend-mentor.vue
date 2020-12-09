<template>
  <div>
    <section id="page-head">
      <h1 class="page-head-title">
        Frontend Mentor Coding Challenges
      </h1>
      <p class="page-head-description">
        A library of my solutions for coding challenges found at <a href="frontendmentor.io" target="_blank">frontendmentor.io</a>
        <br>
        Each website is live and interactive, hosted via <a href="https://vercel.com/" target="_blank">Vercel</a>
      </p>
    </section>

    <section id="codes">
      <Code
        v-for="(code, index) in codes"
        :key="index"
        :link="code.link"
        :imgPath="code.imgPath"
        :caption="code.caption"
      />
    </section>
  </div>
</template>

<script>
import Code from "@/components/Code";

const codes = [
  {
    link: "https://four-card-feature-section-git-master.murerkinn.vercel.app/",
    imgPath: "four-card-feature-section-desktop-design.jpg",
    caption: "Four Card Feature Section"
  },
  {
    link: "https://frontend-mentor-single-price-grid-component-mocha.vercel.app/",
    imgPath: "single-price-grid-component-desktop-design.jpg",
    caption: "Single Price Grid Component"
  },
  {
    link: "https://frontend-mentor-profile-card-component.murerkinn.vercel.app/",
    imgPath: "profile-card-component-desktop-design.jpg",
    caption: "Profile Card Component"
  }
]

export default {
  name: "frontend-mentor",
  components: {
    Code
  },
  data: () => ({
    codes,
  }),
}
</script>
