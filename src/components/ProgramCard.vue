<template>
  <div class="program-card relative mt-2 rounded-2xl shadow-md bg-white">
    <div class="rounded-2xl">
      <img
        class="rounded-t-2xl w-full"
        :src="programDetails.image"
        :alt="programDetails.title + 'image'"
      />
    </div>
    <div class="px-5 mt-3 mb-9">
      <h1 class="text-2xl capitalize text-black font-black">
        {{ programDetails.title }}
      </h1>
    </div>
    <div
      v-html="programDetails.description"
      class="overflow-y-auto h-40 px-5"
    ></div>
    <div class="flex justify-between items-center px-8 my-6">
      <div
        class="flex flex-col items-center justify-center"
        v-for="(detail, index) in programDetails.schedule"
        :key="index"
      >
        <h1 class="program-card-detail-value text-2xl font-extrabold">
          {{ detail.value }}
        </h1>
        <h1 class="capitalize">{{ detail.title }}</h1>
      </div>
    </div>
    <div
      class="program-card-link-div h-auto rounded-b-2xl bottom-0 left-0 right-0 flex justify-center items-center"
    >
      <a
        class="py-5 text-center w-full cursor-pointer"
        :href="programDetails.link['url']"
      >
        <h1 class="text-white font-bold uppercase">
          {{ programDetails.link["text"] }}
        </h1>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProgramCard",
  props: { programDetails: Object },
};
</script>

<style></style>
