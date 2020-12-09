<template>
  <nav class="nav">
    <ul class="menu">
      <li class="menu-item">
        <nuxt-link to="/code" class="menu-link">Code</nuxt-link>
      </li>
      <li class="menu-item">
        <a href="https://www.github.com/murerkinn" class="menu-link" target="_blank">Github</a>
      </li>
      <li class="menu-item">
        <a href="https://www.linkedin.com/in/murat-erkin-cicek" class="menu-link" target="_blank">LinkedIn</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "Menu"
}
</script>

<style lang="scss">
/* Nav Class */
.nav > .menu {
  display: flex;

  .menu-item:not(:last-child) {
    margin-right: 1em;
  }

  .menu-link {
    font-family: 'Josefin Sans', sans-serif;
    font-weight: 300;
    text-transform: uppercase;
    font-size: 13px;
    transition: color 150ms ease-in-out;

    &:hover {
      color: #ff7c5c;
    }
  }
}
</style>
