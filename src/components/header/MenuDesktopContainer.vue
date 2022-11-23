<template>
  <div class="header-desktop-container-menu">
    <ul class="flex justify-center items-center">
      <li
        :class="!styleApply ? 'relative' : 'auto'"
        class="text-center py-3 cursor-pointer"
        v-for="menuItem in menu"
        :key="menuItem.url"
      >
        <MenuDesktopTileContainer
          :menu="menuItem.submenu"
          :styleApply="styleApply"
        />
        <a
          class="capitalize text-center text-lg w-full h-full font-semibold"
          :href="menuItem.url"
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
              d="M5.99962 4.97656L10.1246 0.851562L11.303 
                2.0299L5.99962
                 7.33323L0.696289
                  2.0299L1.87462
                   0.851562L5.99962 4.97656Z"
              fill="#6D6C70"
              data-v-3371b466=""
            ></path>
          </svg>
        </a>
        <div
          v-if="menuItem.has_submenu && !styleApply"
          class="absolute hidden h-max bg-white w-max top-9 bottom-auto shadow-md z-50"
        >
          <ul class="flex flex-col text-gray-800 justify-center items-start">
            <li
              v-for="submenuItem in menuItem.submenu"
              :key="submenuItem.main_title"
              class="border-b relative font-semibold border-gray-400 w-full py-4 px-4"
            >
              <a
                v-if="submenuItem.url != ''"
                :class="
                  submenuItem.url != '' ? 'cursor-pointer' : 'cursor-default'
                "
                class="w-full h-full"
                :href="submenuItem.url"
                >{{ submenuItem.title }}</a
              >
              <span v-else class="cursor-default w-full h-full">{{
                submenuItem.title
              }}</span>
              <div
                style="margin-inline-start: 0.5px"
                class="absolute h-max hidden bg-white w-max top-1 left-full bottom-0 shadow-md z-60"
                v-if="submenuItem.list.length > 0"
              >
                <ul
                  class="flex flex-col text-gray-800 items-center justify-center"
                >
                  <li
                    v-for="listItem in submenuItem.list"
                    :key="listItem.url"
                    class="cursor-pointer border-b font-semibold border-gray-400 w-full py-4 px-4"
                  >
                    <a class="w-full h-full" :href="listItem.url">
                      {{ listItem.title }}</a
                    >
                  </li>
                </ul>
              </div>
            </li>
          </ul>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
import MenuDesktopTileContainer from "./MenuDesktopTileContainer.vue";
export default {
  name: "MenuDesktopContainer",
  props: { menu: Array, styleApply: Boolean },
  components: { MenuDesktopTileContainer },
};
</script>

<style></style>
