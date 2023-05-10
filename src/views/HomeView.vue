<template>
  <div class="home">
    <v-container class="ma-5">
      <v-layout fluid row wrap>
          <v-flex xs12 sm6 md4 lg3 v-for="imageUrl in imageUrls" :key="imageUrl">
            <v-card flat class="text-xs-center ma-3">
              <v-responsive class="pt-4">
                <v-img :src="require('@/assets/component-01/' + imageUrl)" class="ma-2"></v-img>
              </v-responsive>
              <v-card-text>
                <div class="subheading"></div>
                <div class="grey--text"></div>
              </v-card-text>
              <v-card-action>
                <v-btn flat color="grey lighten-4">
                  <v-icon small left>message</v-icon>
                  <span>message</span>
                </v-btn>
              </v-card-action>
            </v-card>
          </v-flex>
      </v-layout>
      <v-layout fluid row wrap>
            <v-flex xs12 sm6 md4 lg3 v-for="imageUrl in imageUrls2" :key="imageUrl">
              <v-card flat class="text-xs-center ma-3">
                <v-responsive class="pt-4">
                  <v-img :src="require('@/assets/component-02/' + imageUrl)" class="ma-2"></v-img>
                </v-responsive>
                <v-card-text>
                  <div class="subheading"></div>
                  <div class="grey--text"></div>
                </v-card-text>
                <v-card-action>
                  <v-btn flat color="grey">
                    <v-icon small left>message</v-icon>
                    <span>message</span>
                  </v-btn>
                </v-card-action>
              </v-card>
              
            </v-flex>
        </v-layout>
      
    </v-container>
    
  </div>
</template>

<script>
export default {
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
      ]
    }
  },
}
</script>
