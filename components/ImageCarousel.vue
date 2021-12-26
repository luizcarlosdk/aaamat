<template>
  <v-carousel hide-delimiters cycle interval="2500">
    <v-carousel-item v-for="(link, i) in photos" :key="link" :src="photos[i]">
    </v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  props: {
    photos: Array,
    required: true,
  },
};
</script>

<style></style>
