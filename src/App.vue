<template>
  <v-app>
    <!-- SIDEBAR -->
    <side-bar
      @selectOption="onSelectOption"
    />

    <v-main>
      <!-- CARDS -->
      <image-gallery :isWithColor="isWithColor"/>
    </v-main>
  </v-app>
</template>

<script setup>
  import SideBar from '@/components/SideBar'
  import ImageGallery from './components/ImageGallery'
  import {ref} from 'vue'

  const isWithColor = ref(true)

  const onSelectOption = (isColor) => {
    isWithColor.value =  isColor
  }
</script>