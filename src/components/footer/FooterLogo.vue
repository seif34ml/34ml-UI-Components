<template>
  <div class="w-1/3 h-full">
    <img class="w-full h-full" :src="logo" alt="logo" srcset="" />
  </div>
</template>

<script>
export default {
  name: "FooterLogo",
  props: {
    logo: String,
  },
};
</script>

<style></style>
