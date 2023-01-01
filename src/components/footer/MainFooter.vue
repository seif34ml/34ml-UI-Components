<template>
  <nav>
    <FooterDesktop
      class="hidden lg:flex"
      :menu="footerOptions.menu"
      :logo="footerOptions.logo"
      :AppStore="footerOptions.AppStore"
      :socialMedia="footerOptions.socialMedia"
      :copyrightHtml="footerOptions.copyrightHtml"
    />
    <!-- <FooterMobile
      class="flex lg:hidden"
      :menu="footerOptions.menu"
      :burgerIcon="footerOptions.mobile_hamburger_menu_icon"
      :logo="footerOptions.logo"
      :styleApply="footerOptions.menu_submenu_style"
      :cart="footerOptions.cart"
      :languages="footerOptions.languageOptions"
    /> -->
  </nav>
</template>

<script>
import FooterDesktop from "./FooterDesktop.vue";
// import HeaderMobile from "./HeaderMobile.vue";
export default {
  name: "MainHeader",
  components: {
    FooterDesktop, //HeaderMobile
  },
  props: {
    footerOptions: Object,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
