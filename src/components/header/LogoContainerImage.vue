<template>
  <div class="header-desktop-container-img">
    <img :src="logo" alt="logo" />
  </div>
</template>

<script>
export default {
  name: "LogoContainerImage",
  props: {
    logo: String,
  },
};
</script>

<style></style>
