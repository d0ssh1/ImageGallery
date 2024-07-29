<script setup>
  import {defineEmits} from 'vue';

  const emits = defineEmits(['selectOption'])

  const selectOption = (isColor) => {
    emits('selectOption', isColor);
  }
</script>

<template>
  <v-navigation-drawer
    expand-on-hover
    rail>
    <v-list>
      <v-list-item
          prepend-avatar="https://avatars.githubusercontent.com/u/109642808?v=4"
          subtitle="d0shi@mail.ru"
          title="Artem Orlov"
      ></v-list-item>
    </v-list>

    <v-divider/>
    <v-list density="compact" nav>
      <v-list-item
        prepend-icon="mdi-image"
        title="Color Gallery"
        value="color"
        @click="selectOption(true)"
      />
      <v-list-item
          prepend-icon="mdi-camera"
          title="Gray Space Gallery"
          value="color"
          @click="selectOption(false)"
      />
    </v-list>
  </v-navigation-drawer>
</template>

<style scoped>

</style>