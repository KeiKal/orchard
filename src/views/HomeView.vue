<template>
  <div class="home">
    <v-container class="ma-5">
      <v-layout fluid row wrap>
            <v-flex xs12 sm12 md6 lg4 v-for="imageUrl in imageUrls2" :key="imageUrl">
              <v-card class="text-xs-center ma-3" flat>
                <v-responsive class="pt-4" @click="showPopup= true">
                  <v-img :src="require('@/assets/component-02/' + imageUrl)" class="hovered"></v-img>
                </v-responsive>
                <v-card-text>
                  <div class="subheading">{{ imageUrl }}</div>
                  <div class="grey--text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum officiis, officia debitis dicta atque hic iusto sit in fugit? Consectetur laborum cupiditate pariatur est blanditiis doloribus, quidem molestias tempora autem.</div>
                </v-card-text>
                <v-row class="ma-5">
                  <Popup />
                  <v-spacer></v-spacer>
                  <v-icon right color="green">recommend</v-icon>
                </v-row>
              </v-card>
              <div v-if="showPopup" class="popup" @click="showPopup = false">
                <v-img :src="require('@/assets/component-02/' + imageUrl)"></v-img>
              </div>
            </v-flex>
            
        </v-layout>
        <v-layout row wrap fluid>
            <v-flex xs12 sm12 md6 lg4 v-for="imageUrl in imageUrls" :key="imageUrl">
              <v-card class="text-xs-center ma-3" flat>
                <v-responsive class="pt-4" @click="showPopup = true">
                  <v-img :src="require('@/assets/component-01/' + imageUrl)" class="hovered"></v-img>
                </v-responsive>
                <v-card-text>
                  <div class="subheading">{{ imageUrl }}</div>
                  <div class="grey--text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam sint autem officiis veniam quas tempora et illum laborum sapiente quaerat odio, earum eligendi facere exercitationem nobis natus quo omnis cupiditate?</div>
                </v-card-text>
                  <v-row class="ma-5">
                    <Popup />
                    <v-spacer></v-spacer>
                    <v-icon right color="green">recommend</v-icon>
                  </v-row>
              </v-card>
              <div v-if="showPopup" class="popup" @click="showPopup = false">
                <v-img :src="require('@/assets/component-01/' + imageUrl)"></v-img>
              </div>
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
      showPopup: false
    }
  }
}
</script>

<style>
.popup{
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.7);
  z-index: 9999;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: auto;
}

.hovered:hover {
  transform: scale(1.05);
  transition: .3s;
}

.hovered {
  transform: scale(1);
  transition: .3s;
}

.popup img {
  max-width: 90%;
  max-height: 90%;
}
</style>