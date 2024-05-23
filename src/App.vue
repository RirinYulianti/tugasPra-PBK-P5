<template>
  <q-layout>
    <div class="nav">
      <Navbar :title="navbarTitle" :navItems="navbarItems" />
    </div>
    <q-page-container>
      <Carousel  />
      <div class="card q-pa-md q-gutter-md row">
        <ProductCard
          v-for="(product, index) in products"
          :key="index"
          :title="product.title"
          :price="product.price"
          :image="product.image"
        />
      </div>
    </q-page-container>
    <Footer :text="footerText" :backgroundColor="footerBackgroundColor" />
  </q-layout>
</template>

<script>
import { QLayout, QPageContainer } from 'quasar'
import Navbar from './components/Navbar.vue'
import ProductCard from './components/ProductCard.vue'
import Footer from './components/Footer.vue' 
import Carousel from './components/Carousel.vue'

export default {
  components: {
    QLayout,
    QPageContainer,
    Navbar,
    ProductCard,
    Footer,
    Carousel
  },
  data() {
    return {
      navbarTitle: 'ZALORA',
      navbarItems: [
        { label: 'Home', link: '#' },
        { label: 'Products', link: '#' },
        { label: 'Contact', link: '#' }
      ],
      products: [
        { title: 'Kaos polos V -neck cewe.', price: 'Rp16.170', image: 'https://down-id.img.susercontent.com/file/34a88047f22f447c0129d1ae481f9674' },
        { title: 'SWEATER PREMIUM', price: 'Rp135.000', image: 'https://down-id.img.susercontent.com/file/id-11134207-7qukw-ljguferjfn4o12' },
        { title: '[ Marveile ] Genevie Dress / Dress Wanita', price: 'Rp239.000', image: 'https://down-id.img.susercontent.com/file/id-11134201-7r98q-luncd5qiojjwa4' },
        { title: 'Unq kaftan cotton dress', price: 'Rp104.000', image: 'https://down-id.img.susercontent.com/file/id-11134207-7r98r-ltf41dvphdad0e' },
        { title: 'Unq kaftan cotton dress', price: 'Rp104.000', image: 'https://down-id.img.susercontent.com/file/id-11134207-7r98r-ltf41dvphdad0e' },
        { title: 'Momelca Syabel Kaftan Wanita', price: 'Rp132.000', image: 'https://down-id.img.susercontent.com/file/sg-11134201-7rceo-lsi4b14hdye832' },
        { title: 'Giordano Poplin Dress', price: 'Rp349.000', image: 'https://down-id.img.susercontent.com/file/aba442cc0beeedd2522579b80046050c' },
        { title: 'Nomitees Vania Dress ', price: 'Rp157.000', image: 'https://down-id.img.susercontent.com/file/id-11134207-7r98o-ll08pwjxdtgg81' }
      ],
      footerText: '&copy; 2024 Toko Online. All Rights Reserved.',
      footerBackgroundColor: '#333'
     
    }
  }
}
</script>

<style>
.nav {
  position: relative;
  z-index: 100;
}
.card {
  width: 100%;
  margin-left: 80px;
}
</style>
