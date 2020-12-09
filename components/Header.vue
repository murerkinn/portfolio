<template>
  <header>
    <nuxt-link to="/" class="logo">mec.</nuxt-link>
    <Menu />
  </header>
</template>

<script>
import Menu from "@/components/Menu";

export default {
  name: "Header",
  components: {
    Menu
  }
}
</script>
