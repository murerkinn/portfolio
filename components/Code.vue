<template>
  <div class="code">
    <a class="code-link" :href="link" target="_blank">
      <img class="code-img" :src="`img/frontend-mentor/${imgPath}`" :alt="caption">
    </a>
    <p class="caption">{{ caption }}</p>
  </div>
</template>

<script>
export default {
  name: "Code",
  props: {
    link: {
      type: String,
      required: true
    },
    imgPath: {
      type: String,
      required: true
    },
    caption: {
      type: String,
      required: true
    }
  }
}
</script>
