<template>
  <footer>
    <p class="copyright">&copy; 2020 | Created by Murat Erkin Cicek</p>
    <Menu />
  </footer>
</template>

<script>
import Menu from "@/components/Menu";

export default {
  name: "Footer",
  components: {
    Menu
  }
}
</script>

<style lang="scss">
/* Footer */
footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1em 0;

  .copyright {
    font-family: 'Josefin Sans', sans-serif;
    font-weight: 300;
    text-transform: uppercase;
    font-size: 13px;
  }
}
</style>
