<template>
  <div class="home">
    <v-container class="ma-5">
      <v-layout fluid row wrap>
            <v-flex xs12 sm6 md6 lg4 v-for="imageUrl in imageUrls2" :key="imageUrl">
              <v-card class="text-xs-center ma-3" flat>
                <v-responsive class="pt-4">
                  <v-img :src="require('@/assets/component-02/' + imageUrl)"></v-img>
                </v-responsive>
                <v-card-text>
                  <div class="subheading"></div>
                  <div class="grey--text"></div>
                </v-card-text>
                  <v-btn small color="grey--text" @click="openPopup">View</v-btn>
                  <popup></popup>
              </v-card>
              
            </v-flex>
        </v-layout>
        <v-layout row wrap fluid>
            <v-flex xs12 sm12 md6 lg4 v-for="imageUrl in imageUrls" :key="imageUrl">
              <v-card class="text-xs-center ma-3" flat>
                <v-responsive class="pt-4">
                  <v-img :src="require('@/assets/component-01/' + imageUrl)"></v-img>
                </v-responsive>
                <v-card-text>
                  <div class="subheading"></div>
                  <div class="grey--text"></div>
                </v-card-text>
                  <v-btn small color="grey--text" @click="openPopup">View</v-btn>
                  <popup></popup>
              </v-card>
            </v-flex>
        </v-layout>
      
    </v-container>
    
  </div>
</template>

<script>

import Popup from '@/components/Popup.vue';
export default {
  components: {
    Popup
  },
  methods: {
    openPopup() {
      this.$refs.el.Popup.openDialog()
    }
  },
  data() {
    return {
      imageUrls: [
        'Image-01.jpg',
        'Image-02.jpg',
        'Image-03.jpg',
      ],
      imageUrls2: [
        'Image-01.jpg',
        'Image-02.jpg',
        'Image-03.jpg',
      ],
      isHovered : false
    }
  },
}
</script>

