<script setup>
const props = defineProps({
  images: {
    type: Array,
    required: true,
  },
});
</script>

<template>
  <div class="mt-8 grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
    <div
      v-for="image in props.images"
      :key="image.src"
      class="group overflow-hidden rounded-2xl bg-white"
    >
      <img
        :src="image.src"
        :alt="image.alt"
        class="h-44 w-full object-cover transition duration-500 group-hover:scale-105"
      />
    </div>
  </div>
</template>

<style scoped></style>
