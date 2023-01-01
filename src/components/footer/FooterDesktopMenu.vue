<template>
  <div class="flex justify-between">
    <div class="mr-4" v-for="(mainItem, index) in menu" :key="index">
      <span class="mb-10 font-extrabold text-lg text-white capitalize">{{
        mainItem.title
      }}</span>
      <ul class="mt-10">
        <li
          class="mb-3 text-white"
          v-for="(itemList, index) in mainItem.list"
          :key="index"
        >
          <a :href="itemList.url">
            {{ itemList.title }}
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterDesktopMenu",
  props: { menu: Array },
};
</script>

<style></style>
