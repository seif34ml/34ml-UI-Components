<template>
  <div
    class="relative flex flex-col footer-desktop-container px-10 py-2 shadow-md items-start justify-between pt-10 pb-8"
  >
    <FooterLogo :logo="getImgSrc" />
    <footer-mobile-menu :menu="menu" />
    <footer-desktop-app-store
      :appStoreImage="appStoreImages"
      :appStore="AppStore"
    ></footer-desktop-app-store>
    <footer-desktop-social
      :socialImages="socialImages"
      :socialMedia="socialMedia"
    >
      <template>
        <span class="text-white capitalize font-extrabold">Follow us</span>
      </template>
    </footer-desktop-social>
    <footer-desktop-copy-rights
      :copyrightHtml="copyrightHtml"
    ></footer-desktop-copy-rights>
  </div>
</template>

<script>
import FooterLogo from "./FooterLogo.vue";
import FooterMobileMenu from "./FooterMobileMenu.vue";
import FooterDesktopAppStore from "./FooterDesktopAppStore.vue";
import FooterDesktopSocial from "./FooterDesktopSocial.vue";
import FooterDesktopCopyRights from "./FooterDesktopCopyRights.vue";

export default {
  name: "FooterMobile",
  components: {
    FooterLogo,
    FooterMobileMenu,
    FooterDesktopAppStore,
    FooterDesktopSocial,
    FooterDesktopCopyRights,
  },
  props: {
    logo: String,
    menu: Array,
    AppStore: Array,
    socialMedia: Array,
    copyrightHtml: String,
  },
  data() {
    return {
      appStoreImages: [],
      socialImages: [],
    };
  },
  mounted() {
    this.AppStore.forEach((item) => {
      this.appStoreImages.push(require("../../assets/" + item.img));
    });
    this.socialMedia.forEach((item) => {
      this.socialImages.push(require("../../assets/" + item.img));
    });
  },
  computed: {
    getImgSrc() {
      return require("../../assets/" + this.logo);
    },
  },
};
</script>

<style></style>
