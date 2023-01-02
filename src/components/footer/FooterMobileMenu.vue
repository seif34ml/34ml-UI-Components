<template>
  <div>
    <ul>
      <li
        class="footer-mobile-menu mt-3 font-bold text-lg text-white capitalize"
        v-for="menuItem in menu"
        :key="menuItem.title"
      >
        {{ menuItem.title }}
        <svg
          v-if="menuItem.list.length > 0"
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

        <ul class="mt-1 mb-1 px-4 footer-mobile-submenu">
          <li
            class="font-medium text-base"
            v-for="listItem in menuItem.list"
            :key="listItem.title"
          >
            <a :href="listItem.url">{{ listItem.title }}</a>
          </li>
        </ul>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "FooterMobileMenu",
  props: { menu: Array },
  data() {
    return {
      showMenus: [],
    };
  },
  mounted() {
    this.showMenus.length = this.menu.length;
    this.showMenus.fill(true);
  },
  methods: {
    showSubMenu(idx) {
      this.showMenus.forEach((m, index) => {
        idx == index
          ? (this.showMenus[index] = true)
          : (this.showMenus[index] = false);
      });
    },
  },
};
</script>

<style></style>
