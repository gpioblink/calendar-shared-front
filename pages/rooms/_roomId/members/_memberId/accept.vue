<template>
    <v-row justify="center">
      <v-col cols="12" sm="6">
        <v-card>
          <v-card-title>〇〇ルームに✕✕さんが参加しようとしています</v-card-title>
          <v-card-text>
            <v-card
                outlined
            >
                <v-list-item three-line>
                <v-list-item-content>
                    <v-list-item-title class="text-h5 mb-1">
                    じぶりん
                    </v-list-item-title>
                    <v-list-item-subtitle class="wrap-text text-wrap">あああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああいいいいいいいいいいいいいいいいいいいいいいいいうううううううううううううううううえええ</v-list-item-subtitle>
                </v-list-item-content>

                <v-list-item-avatar
                    tile
                    size="80"
                    color="grey"
                >
                <v-img src="https://cdn.vuetifyjs.com/images/profiles/marcus.jpg"></v-img>
                </v-list-item-avatar>
                </v-list-item>
            </v-card>
            <div class="my-4"></div>
            <p>承認しますか？</p>
            <v-btn color="primary">承認する</v-btn>
            <v-btn class="mx-3">断る</v-btn>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </template>
  
  <script>
  export default {
    name: 'UserIntegrationPage',
    layout: 'room'
  }
  </script>

<style scoped>
.wrap-text {
   -webkit-line-clamp: unset !important;
}
</style>