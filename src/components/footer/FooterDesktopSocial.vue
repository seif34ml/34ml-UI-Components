<template>
  <div>
    <slot></slot>
    <ul class="flex mt-4">
      <li v-for="(item, index) in socialMedia" class="mr-4" :key="index">
        <a :href="item.url">
          <img :src="socialImages[index]" alt="follow us" />
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "FooterDesktopSocial",
  props: { socialImages: Array, socialMedia: Array },
};
</script>

<style></style>
