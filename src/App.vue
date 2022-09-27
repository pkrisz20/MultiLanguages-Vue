<template>
  <div id="app">
    <div id="nav">
      <router-link :to="`/${$i18n.locale}`">Home</router-link> |
      <router-link :to="`/${$i18n.locale}/about`">About</router-link>
    </div>
    <LanguageSwitcher />
    <router-view/>
  </div>
</template>

<script>
import LanguageSwitcher from "@/components/LanguageSwitcher.vue";

export default {
  name: "App",
  components: {
    LanguageSwitcher
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
