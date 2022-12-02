<script>
import TopSection from "@/components/TopSection.vue";
import BottomSection from "@/components/BottomSection.vue";

export default {
  components: {
    TopSection,
    BottomSection,
  },
};
</script>
<template>
  <div class="container-fluid">
    <TopSection />
    <BottomSection />
  </div>
</template>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
