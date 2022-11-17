<template>
  <div
    class="header-desktop-container px-20 py-2 shadow-md items-center justify-between"
  >
    <div class="header-desktop-container-img">
      <img :src="getImgSrc" alt="logo" />
    </div>
    <div class="header-desktop-container-menu">
      <ul class="flex justify-center items-center">
        <li class="" v-for="menuItem in menu" :key="menuItem.url">
          <a class="capitalize text-lg font-semibold" :href="menuItem.url"
            >{{ menuItem.main_title }}
            <svg
              v-if="menuItem.has_submenu"
              width="12"
              height="8"
              viewBox="0 0 12 8"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
              class="inline-block"
              data-v-3371b466=""
            >
              <path
                d="M5.99962 4.97656L10.1246 0.851562L11.303 2.0299L5.99962 7.33323L0.696289 2.0299L1.87462 0.851562L5.99962 4.97656Z"
                fill="#6D6C70"
                data-v-3371b466=""
              ></path>
            </svg>
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeaderDesktop",
  props: {
    logo: String,
    menu: Array,
  },
  computed: {
    getImgSrc() {
      return require("../../assets/" + this.logo);
    },
  },
};
</script>

<style></style>
