<template>
  <div>
    <select
      :value="languages.selectedLanguage"
      @change="changeLanguage($event.target.value)"
    >
      <option
        v-for="lang in languages.languages"
        :key="lang.code"
        :value="lang.code"
      >
        {{ lang.languageName }}
      </option>
    </select>
  </div>
</template>
<script>
export default {
  name: "LocalizationContainer",
  props: { languages: Object },
  methods: {
    emitChangeLanguage(event) {
      this.$emit("changeLanguage", event);
    },
  },
};
</script>

<style></style>
