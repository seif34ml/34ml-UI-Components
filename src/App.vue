<template>
  <div id="app">
    <div class="grid grid-cols-3">
      <ProgramCard :programDetails="programDetails" />
    </div>
  </div>
</template>

<script>
import ProgramCard from "./components/ProgramCard.vue";
export default {
  name: "App",
  components: { ProgramCard },
  data() {
    return {
      HeaderOptions: {
        logo: "logo.png",
        menu: [
          {
            main_title: "magazine",
            url: "read",
            has_submenu: true,
            mobile_submenu: true,
            mobile_url: "read",
            submenu: [
              {
                title: "pregnancy test",
                url: "read/categories/pregnancy",
                list: [
                  { title: "Mums", url: "read/categories/pregnancy/mums" },
                ],
              },
              {
                title: "parent",
                url: "",
                list: [{ title: "sub", url: "read/categories/parent/sub" }],
              },
              {
                title: "test test",
                url: "read/categories/test-test",
                list: [
                  {
                    title: "Test subcategory",
                    url: "read/categories/test-test/test-subcategory",
                  },
                ],
              },
              {
                title: "Child",
                url: "read/categories/child",
                list: [
                  {
                    title: "Baby Development",
                    url: "read/categories/child/baby-development",
                  },
                ],
              },
            ],
          },
          {
            main_title: "watch",
            url: "watch",
            has_submenu: true,
            mobile_submenu: true,
            mobile_url: "watch",
            submenu: [
              {
                title: "Series",
                url: "watch/series",
                list: [
                  {
                    title: "why moms love murder1",
                    url: "watch/series/why-moms-love-murder1",
                  },
                  {
                    title: "why moms love murder2",
                    url: "watch/series/why-moms-love-murder2",
                  },
                  {
                    title: "donot start your own business: a series",
                    url: "watch/series/donot-start-your-own-business-a-series",
                  },
                  { title: "rrrkl", url: "watch/series/rrrkl" },
                  {
                    title: "why moms love murder3",
                    url: "watch/series/why-moms-love-murder3",
                  },
                  {
                    title: "Success stories every mother should know",
                    url: "watch/series/success-stories-every-mother-should-know",
                  },
                  {
                    title: "Your guide to entrepreneurship as a mom",
                    url: "watch/series/your-guide-to-entrepreneurship-as-a-mom",
                  },
                  {
                    title: "workout, eat healthy, stay happy",
                    url: "watch/series/workout-eat-healthy-stay-happy",
                  },
                  {
                    title: "how to talk so teens can listen",
                    url: "watch/series/how-to-talk-so-teens-can-listen",
                  },
                ],
              },
              {
                title: "Videos",
                url: "watch/videos",
                list: [
                  {
                    title: "pregnancy test",
                    url: "watch/categories/pregnancy",
                  },
                ],
              },
            ],
          },
          {
            main_title: "shop",
            url: "products",
            has_submenu: false,
            mobile_submenu: false,
            submenu: [],
          },
          {
            main_title: "get fit",
            url: "fit-programs",
            has_submenu: false,
            mobile_submenu: false,
            submenu: [],
          },
          {
            main_title: "card",
            url: "card",
            has_submenu: false,
            mobile_submenu: false,
            submenu: [],
          },
          {
            main_title: "events",
            url: "events",
            has_submenu: false,
            mobile_submenu: false,
            submenu: [],
          },
          {
            main_title: "about",
            url: "about-us",
            has_submenu: true,
            mobile_submenu: true,
            submenu: [
              { title: "about us", url: "about-us", list: [] },
              { title: "contact us", url: "contact-us", list: [] },
              {
                title: "advertise with us",
                url: "advertise-with-us",
                list: [],
              },
              { title: "frequently asked questions", url: "/faqs", list: [] },
              {
                title: "terms & conditions",
                url: "pages/terms/content",
                list: [],
              },
              {
                title: "privacy policy",
                url: "pages/privacy-policy/content",
                list: [],
              },
            ],
          },
        ],
        menu_submenu_style: true,
        cart: {
          count: 0,
          url: "/",
          image: "cart-icon.svg",
        },
        languageOptions: {
          selectedLanguage: "en",
          languages: [
            { languageName: "En", code: "en" },
            { languageName: "ع", code: "ar" },
          ],
        },
        mobile_hamburger_menu_icon: "burger.webp",
      },
      footerOptions: {
        logo: "footerlogo.png",
        menu: [
          {
            title: "magazine",
            list: [
              { title: "read", url: "read" },
              { title: "watch", url: "watch" },
              { title: "confess", url: "confessions" },
              { title: "quizzes", url: "quizzes" },
            ],
          },
          {
            title: "shop",
            list: [
              { title: "shop", url: "products" },
              { title: "rahet bally card", url: "card" },
              { title: "card catalouge", url: "merchants" },
            ],
          },
          {
            title: "experience",
            list: [
              { title: "get fit", url: "fit-programs" },
              { title: "events", url: "events" },
            ],
          },
          {
            title: "about us",
            list: [
              { title: "about us", url: "about-us" },
              { title: "contact us", url: "contact-us" },
              { title: "advertise with us", url: "advertise-with-us" },
              { title: "frequently asked questions", url: "faqs" },
              { title: "terms & conditions", url: "pages/terms/content" },
              {
                title: "privacy policy",
                url: "pages/privacy-policy/content",
              },
              { title: "sitemap", url: "sitemap" },
            ],
          },
        ],
        AppStore: [
          {
            img: "play-store-sm.webp",
            url: "https://keepersecurity.eu/vault/",
          },
          { img: "app-store-sm.webp", url: "https://keepersecurity.eu/vault/" },
        ],
        socialMedia: [
          { img: "facebook-footer-icon.webp", url: "https://facebook.com" },
          { img: "instagram-footer-icon.webp", url: "https://instagram.com" },
          { img: "facebook-footer-icon.webp", url: "https://facebook.com" },
          { img: "instagram-footer-icon.webp", url: "https://instagram.com" },
          { img: "facebook-footer-icon.webp", url: "https://facebook.com" },
          { img: "facebook-footer-icon.webp", url: "https://facebook.com" },
        ],
        copyrightHtml:
          '<p class="text-white font-montserrat-medium text-xs mt-6" data-v-3254ec04="">© Rahet Bally 2022 | All Rights Reserved | Designed By<a href="https://34ml.com" target="_blank" class="font-montserrat-bold">[34]ML</a></p>',
      },
      programDetails: {
        image:
          "https://rahet-bally-production.s3.eu-central-1.amazonaws.com/22455/conversions/fitmama-Program%27s-image-thumbnail_d_webp.webp?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIA3JCVZFIK6BEJFN5N%2F20230111%2Feu-central-1%2Fs3%2Faws4_request&X-Amz-Date=20230111T133149Z&X-Amz-SignedHeaders=host&X-Amz-Expires=172800&X-Amz-Signature=289f62dca83295edc01fc7bcf65b14df62e0121f7b41336906f77c656ecc6509",
        title: "fit-mama",
        description:
          "<div>- Program focuses on strengthening the body &amp; building endurance&nbsp;<br>- Nutrition Plan (Optional) updated weekly&nbsp;<br>- Supported by FREE babysitting services</div>",
        schedule: [
          { title: "session", value: "14" },
          { title: "week", value: "4" },
          { title: "per session", value: "3hrs" },
        ],
        link: {
          url: "/",
          text: "view details",
        },
      },
    };
  },
};
</script>

<style></style>
