<template>
  <div class="container-fluid">
    <TopSection />
  </div>
</template>
<script>
import TopSection from "@/components/TopSection.vue";

export default {
  components: {
    TopSection,
  },
};
</script>
<style>
h1 {
  color: white;
}
p {
  color: white;
}
.container-fluid {
  background-color: black;
  color: #50a65e;
}
</style>
