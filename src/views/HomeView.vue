<template>
  <div class="home">
    <div v-for="imageUrl in imageUrls" :key="imageUrl">
        <v-img :src="require('@/assets/component-01/' + imageUrl)" ></v-img>
      </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      imageUrls: [
        'Image-01.jpg',
        'Image-02.jpg',
      ]
    }
  },
}
</script>
