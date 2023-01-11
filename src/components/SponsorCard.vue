<template>
  <div
    class="bg-white rounded-xl sponsor-card w-44 h-44 flex justify-center items-center shadow-lg"
  >
    <div class="w-3/4 h-3/4">
      <img :src="sponsorDetails.image" :alt="sponsorDetails.title" />
    </div>
  </div>
</template>

<script>
export default {
  name: "SponsorCard",
  props: { sponsorDetails: Object },
};
</script>

<style></style>
