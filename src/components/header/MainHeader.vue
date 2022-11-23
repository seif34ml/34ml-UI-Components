<template>
  <nav>
    <HeaderDesktop
      class="hidden lg:flex"
      :menu="HeaderOptions.menu"
      :logo="HeaderOptions.logo"
      :styleApply="HeaderOptions.menu_submenu_style"
      :cart="HeaderOptions.cart"
      :languages="HeaderOptions.languageOptions"
    />
    <HeaderMobile
      class="flex lg:hidden"
      :menu="HeaderOptions.menu"
      :burgerIcon="HeaderOptions.mobile_hamburger_menu_icon"
      :logo="HeaderOptions.logo"
      :styleApply="HeaderOptions.menu_submenu_style"
      :cart="HeaderOptions.cart"
      :languages="HeaderOptions.languageOptions"
    />
  </nav>
</template>

<script>
import HeaderDesktop from "./HeaderDesktop.vue";
import HeaderMobile from "./HeaderMobile.vue";
export default {
  name: "MainHeader",
  components: { HeaderDesktop, HeaderMobile },
  props: {
    HeaderOptions: Object,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
