<script setup>
import Navbar from "./components/Navbar.vue";
import SearchBar from "./components/SearchBar.vue";
import UploadButton from "./components/UploadButton.vue";
import GalleryGrid from "./components/GalleryGrid.vue";

const images = [
  {
    src: "https://images.unsplash.com/photo-1487412720507-e7ab37603c6f?auto=format&fit=crop&w=900&q=80",
  },
  {
    src: "https://images.unsplash.com/photo-1501183638710-841dd1904471?auto=format&fit=crop&w=900&q=80",
  },
  {
    src: "https://images.unsplash.com/photo-1489515217757-5fd1be406fef?auto=format&fit=crop&w=900&q=80",
  },
  {
    src: "https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=900&q=80",
  },
  {
    src: "https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?auto=format&fit=crop&w=900&q=80",
  },
  {
    src: "https://images.unsplash.com/photo-1523413651479-597eb2da0ad6?auto=format&fit=crop&w=900&q=80",
  },
];
</script>

<template>
  <div class="min-h-screen">
    <div class="mx-auto max-w-5xl px-6 pb-16 pt-10">
      <Navbar />

      <div class="mt-10 flex flex-wrap items-center justify-between gap-6">
        <SearchBar />
        <UploadButton />
      </div>

      <GalleryGrid :images="images" />
    </div>
  </div>
</template>

<style scoped></style>
