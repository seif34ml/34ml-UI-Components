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
    <FooterMobile
      class="flex lg:hidden"
      :menu="footerOptions.menu"
      :logo="footerOptions.logo"
      :AppStore="footerOptions.AppStore"
      :socialMedia="footerOptions.socialMedia"
      :copyrightHtml="footerOptions.copyrightHtml"
    />
  </nav>
</template>

<script>
import FooterDesktop from "./FooterDesktop.vue";
import FooterMobile from "./FooterMobile.vue";
export default {
  name: "MainHeader",
  components: {
    FooterDesktop,
    FooterMobile,
  },
  props: {
    footerOptions: Object,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
