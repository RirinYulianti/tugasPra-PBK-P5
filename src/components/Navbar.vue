<template>
  <q-header elevated :class="$q.dark.isActive ? 'bg-primary' : 'bg-black'">
    
    <q-toolbar>
      <q-btn ro dense @click="toggleDrawer" icon="menu" />
      <q-toolbar-title class="titel">ZALORA</q-toolbar-title>
      <q-drawer v-model="showDrawer" :side="drawerSide" round dense content-class="drawer-content">
          <q-tabs v-model="showDrawer">
            <q-tab class="drawer-item" v-for="(item, index) in drawerItems" :key="index"  :label="item.label" :icon="item.icon" />
          </q-tabs>
      </q-drawer>
      <q-btn flat label="Home" />
      <q-btn flat label="Products" />
      <q-btn flat label="Contact" />
      <q-space />
      <q-btn flat dense icon="shopping_cart" @click="toggleCart" />
      <q-badge v-if="cartItems.length > 0" color="primary">{{ cartItems.length }}</q-badge>
    </q-toolbar>
  </q-header>
</template>

<script setup>
import { ref } from 'vue'
import { QHeader, QToolbar, QToolbarTitle, QBtn, QSpace, QBadge, QDrawer, QScrollArea, QTabs, QTab } from 'quasar'

const showDrawer = ref(false)
const cartItems = ref([])
const drawerSide = 'left'

const drawerItems = [
  { label: 'Avatar', icon: 'person' },
  { label: 'Setting Account', icon: 'settings' },
  { label: 'Payment', icon: 'payment' },
  { label: 'Feedback', icon: 'feedback' },
  { label: 'Help', icon: 'help' },
  { label: 'Logout', icon: 'exit_to_app' }
]

const toggleCart = () => {
  // Implement toggle logic for cart here
}

const toggleDrawer = () => {
  showDrawer.value = !showDrawer.value
}

const selectDrawerItem = (index) => {
  // Handle selecting drawer item here
  console.log('Selected drawer item:', drawerItems[index])
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;0,700;1,300;1,400;1,500;1,600;1,700&display=swap');

.drawer-content {
  width: 250px;
}

.drawer-item {
  color: black;
}

.titel{
  font-weight: bold;
  font-family: "Cormorant Garamond", serif;
}
</style>
