<template>
  <div class="header-mobile-container-menu">
    <div @click="showMenu = true" v-show="!showMenu">
      <img class="w-10 h-10" :src="burgerIcon" alt="" />
    </div>

    <div
      v-show="showMenu"
      class="z-50 px-6 py-10 header-mobile-container-menu-tile -left-2 absolute h-screen w-10/12 flex flex-col bg-white top-0"
    >
      <div class="w-full flex flex-row justify-between">
        <slot> </slot>
        <LocalizationContainer :languages="languages" />
      </div>
      <ul class="mt-8 font-semibold">
        <li
          @click="toggleIndex(index)"
          v-for="(menuItem, index) in menu"
          class="mt-3"
          :key="menuItem.url"
        >
          {{ menuItem.main_title }}

          <svg
            v-if="menuItem.submenu.length > 0"
            width="12"
            height="8"
            viewBox="0 0 12 8"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
            class="inline-block"
            data-v-3371b466=""
          >
            <path
              d="M5.99962 4.97656L10.1246 0.851562L11.303 
                2.0299L5.99962
                 7.33323L0.696289
                  2.0299L1.87462
                   0.851562L5.99962 4.97656Z"
              fill="#6D6C70"
              data-v-3371b466=""
            ></path>
          </svg>
          <ul
            class="px-3 font-normal"
            v-show="menuItem.submenu.length && menuShowSelectedIndex === index"
          >
            <li
              class="mt-2"
              v-for="(submenuItems, subindex) in menuItem.submenu"
              :key="submenuItems.url"
            >
              <a v-if="submenuItems.url" :href="submenuItems.url">{{
                submenuItems.title
              }}</a>
              <span v-else>{{ submenuItems.title }}</span>
              <svg
                v-if="submenuItems.list.length > 0"
                width="12"
                height="8"
                viewBox="0 0 12 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                class="inline-block"
                data-v-3371b466=""
                @click="toggleSubindex(subindex)"
              >
                <path
                  d="M5.99962 4.97656L10.1246 0.851562L11.303 
                2.0299L5.99962
                 7.33323L0.696289
                  2.0299L1.87462
                   0.851562L5.99962 4.97656Z"
                  fill="#6D6C70"
                  data-v-3371b466=""
                ></path>
              </svg>
              <ul
                class="px-2"
                v-show="
                  submenuItems.list.length > 0 &&
                  menuShowSelectedIndex === index &&
                  listShowIndices === subindex
                "
              >
                <li v-for="itemList in submenuItems.list" :key="itemList.url">
                  <a :href="itemList.url"> {{ itemList.title }}</a>
                </li>
              </ul>
            </li>
          </ul>
        </li>
      </ul>
    </div>
    <div
      v-show="showMenu"
      @click="showMenu = false"
      class="absolute top-0 w-screen h-screen bg-slate-500 bg-opacity-50 z-40"
    ></div>
  </div>
</template>

<script>
import LocalizationContainer from "./header/LocalizationContainer.vue";
export default {
  name: "MobileMenuContainer",
  components: {
    LocalizationContainer,
  },
  props: {
    menu: Array,
    burgerIcon: String,
    languages: Object,
  },
  data() {
    return {
      menuShowSelectedIndex: null,
      listShowIndices: null,
      showMenu: false,
    };
  },
  methods: {
    toggleIndex(index) {
      if (this.menuShowSelectedIndex === index) {
        this.menuShowSelectedIndex = null;
      } else {
        this.menuShowSelectedIndex = index;
      }
    },
    toggleSubindex(sub) {
      if (this.menuShowSelectedIndex === sub) {
        this.listShowIndices = null;
      } else {
        this.listShowIndices = sub;
      }
    },
  },
};
</script>

<style></style>
