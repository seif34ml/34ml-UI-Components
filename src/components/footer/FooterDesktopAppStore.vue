<template>
  <div class="mt-10 mb-10">
    <ul class="flex justify-start">
      <li class="mr-4" v-for="(item, index) in appStore" :key="item.url">
        <a :href="item.url" class="w-14 h-3">
          <img :src="appStoreImage[index]" alt="get the app" />
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "FooterDesktopAppStore",
  props: { appStore: Array, appStoreImage: Array },
};
</script>

<style></style>
