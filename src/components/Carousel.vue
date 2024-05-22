<template>
  <div class="q-pa-md">
    <q-carousel
      animated
      v-model="slide"
      :autoplay="true"
      arrows
      navigation
      infinite
    >
      <q-carousel-slide :name="1" img-src="https://images.pexels.com/photos/20232007/pexels-photo-20232007/free-photo-of-merah-tanda-penanda-isyarat.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" />
      <q-carousel-slide :name="2" img-src="https://images.pexels.com/photos/5650026/pexels-photo-5650026.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" />
      <q-carousel-slide :name="3" img-src="https://images.pexels.com/photos/2460436/pexels-photo-2460436.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" />
      <q-carousel-slide :name="4" img-src="https://images.pexels.com/photos/6347538/pexels-photo-6347538.jpeg?auto=compress&cs=tinysrgb&w=600" />
    </q-carousel>
  </div>
</template>

<script>
import { ref } from 'vue'
import { QCarousel, QCarouselSlide, QIcon } from 'quasar'

export default {
  setup() {
    return {
      slide: ref(1)
    }
  },
  components: {
    QCarousel,
    QCarouselSlide,
    QIcon
  }
}
</script>
