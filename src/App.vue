<script setup>
import SideBar from "./components/SideBar.vue"
import ImageGallery from "@/components/ImageGallery.vue"
import {ref} from "vue"

const isColored = ref(true)
const onSelectOption = (isColor) => {
  isColored.value = isColor
}
</script>

<template>
  <v-app>
    <SideBar @selectOption="onSelectOption"/>
    <v-main>
      <ImageGallery :isColored="isColored"/>
    </v-main>
  </v-app>
</template>
