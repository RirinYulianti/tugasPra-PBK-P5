<template>
  <q-footer elevated :style="{ backgroundColor: backgroundColor }" class="footer">
    <q-toolbar class="footer-toolbar">
      <q-toolbar-title>{{ text }}</q-toolbar-title>
    </q-toolbar>
  </q-footer>
</template>

<script setup>
import { defineProps } from 'vue'

const props = defineProps({
  text: String,
  backgroundColor: String
});
</script>

<style scoped>
.footer-toolbar {
  justify-content: center; /* Memusatkan teks secara horizontal */
  color: white; /* Warna teks putih */
}
.footer {
  width: 100%; /* Memastikan footer melebar penuh */
  position: absolute;
  bottom: 0;
  left: 0;
}

</style>
