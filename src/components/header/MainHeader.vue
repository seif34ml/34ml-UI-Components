<template>
  <nav>
    <HeaderDesktop
      class="hidden lg:flex"
      :menu="HeaderOptions.menu"
      :logo="HeaderOptions.logo"
    />
  </nav>
</template>

<script>
import HeaderDesktop from "./HeaderDesktop.vue";
export default {
  name: "MainHeader",
  components: { HeaderDesktop },
  props: {
    HeaderOptions: Object,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
