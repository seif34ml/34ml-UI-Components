<template>
  <div
    class="header-desktop-container px-20 py-2 shadow-md items-center justify-between"
  >
    <LogoContainerImage :logo="getImgSrc" />
    <MenuDesktopContainer :menu="menu" />
  </div>
</template>

<script>
import MenuDesktopContainer from "./MenuDesktopContainer.vue";
import LogoContainerImage from "./LogoContainerImage.vue";
export default {
  name: "HeaderDesktop",
  props: {
    logo: String,
    menu: Array,
    styleApply: Boolean,
  },
  components: {
    LogoContainerImage,
    MenuDesktopContainer,
  },
  computed: {
    getImgSrc() {
      return require("../../assets/" + this.logo);
    },
  },
};
</script>

<style></style>
