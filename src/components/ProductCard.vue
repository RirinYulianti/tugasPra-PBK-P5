<!-- ProductCard.vue -->

<template>
  <q-card class="product-card">
    <q-card-section class="image-section">
      <q-img class="product-image" :src="image" :alt="title" />
    </q-card-section>
    <q-card-section class="details-section">
      <div class="text-h6">{{ title }}</div>
      <div class="text-subtitle1">{{ price }}</div>
    </q-card-section>
    <q-card-actions class="actions-section">
      <q-btn flat label="Buy Now" color="primary" />
    </q-card-actions>
  </q-card>
</template>

<script setup>
import { defineProps } from 'vue'
import { QCard, QCardSection, QImg, QCardActions, QBtn } from 'quasar'

const props = defineProps({
  title: String,
  price: String,
  image: String
})
</script>

<style scoped>
.product-card {
  width: 300px; /* Menetapkan lebar kartu */
  height: auto; /* Atur ketinggian agar disesuaikan dengan konten */
}

.image-section {
  height: 200px; /* Menetapkan tinggi bagian gambar */
}

.product-image {
  width: 100%; /* Mengisi lebar gambar ke dalam bagian gambar */
  height: 100%; /* Mengisi tinggi gambar ke dalam bagian gambar */
}

.details-section,
.actions-section {
  padding: 1rem; /* Spasi dalam setiap bagian */
}
</style>
