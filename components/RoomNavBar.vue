<template>
    <v-toolbar>
        <v-btn
              icon
              class="hidden-xs-only"
              to="/"
            >
              <v-icon>mdi-arrow-left</v-icon>
        </v-btn>
        <v-toolbar-title>Zliルーム</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-menu bottom left>
            <template v-slot:activator="{ on, attrs }">
              <v-btn icon class="hidden-xs-only" v-bind="attrs" v-on="on">
                <v-icon>mdi-dots-vertical</v-icon>
              </v-btn>
            </template>

            <v-list>
              <v-list-item link>
                <v-list-item-title>ルームに招待</v-list-item-title>
              </v-list-item>
              <v-list-item link>
                <v-list-item-title>管理者向け設定</v-list-item-title>
              </v-list-item>
              <v-list-item link>
                <v-list-item-title>このルームから退出</v-list-item-title>
              </v-list-item>
            </v-list>
        </v-menu>
    </v-toolbar>
</template>
  
  <script lang="ts">
  import Vue from 'vue';
  // import firebase from "firebase";
  
  export default Vue.extend({
    name: 'RoomNavBar',
    methods: {
    },
    mounted() {
    //   firebase.auth().onAuthStateChanged(user => {
    //     if(user) {
    //       this.user = user;
    //     }
    //   });
    },
    data() {
      return {
        searchQuery: this.$route.query.query,
        user: { photoURL: "https://bulma.io/images/placeholders/128x128.png"}
      }
    }
  });
  </script>
  