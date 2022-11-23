<template>
  <div
    v-if="styleApply && menu.length > 0"
    class="cursor-default header-desktop-container-vsa-submenu xl:grid-cols-4 lg:grid-cols-3 hidden w-screen py-8 px-32 top-full bg-white shadow-md absolute"
  >
    <div
      v-for="submenu in menu"
      :key="submenu.title"
      class="cursor-default flex flex-col"
    >
      <a :href="submenu.url">
        <span>{{ submenu.title }}</span>
      </a>
      <ul class="mt-4" v-if="submenu.list.length > 0">
        <li
          v-for="list in submenu.list"
          :key="list.url"
          :href="list.url"
          class="text-gray-800 mt-2"
        >
          <a :href="list.url">{{ list.title }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "MenuDesktopTileContainer",
  props: { menu: Array, styleApply: Boolean },
};
</script>

<style></style>
