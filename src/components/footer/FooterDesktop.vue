<template>
  <div
    class="relative flex footer-desktop-container px-20 py-2 shadow-md items-start justify-between pt-10 pb-16"
  >
    <div class="block w-1/3">
      <footer-logo :logo="getImgSrc"></footer-logo>
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
    <div class="block w-2/3">
      <footer-desktop-menu :menu="menu" />
    </div>
  </div>
</template>

<script>
import FooterLogo from "./FooterLogo.vue";
import FooterDesktopAppStore from "./FooterDesktopAppStore.vue";
import FooterDesktopSocial from "./FooterDesktopSocial.vue";
import FooterDesktopMenu from "./FooterDesktopMenu.vue";
import FooterDesktopCopyRights from "./FooterDesktopCopyRights.vue";

export default {
  name: "FooterDesktop",
  components: {
    FooterLogo,
    FooterDesktopAppStore,
    FooterDesktopSocial,
    FooterDesktopMenu,
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
  // components: {
  //   // LogoContainerImage,
  //   // MenuDesktopContainer,
  //   // CartContainer,
  //   // LocalizationContainer,
  // },
  computed: {
    getImgSrc() {
      return require("../../assets/" + this.logo);
    },
  },
};
</script>

<style>
.footer-desktop-container {
  background-color: #00abeb;
}
</style>
