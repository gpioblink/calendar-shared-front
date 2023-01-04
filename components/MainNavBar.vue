<template>
    <v-toolbar>
        <v-toolbar-title @click="$router.push('/')" style="cursor:pointer">みんなのカレンダー</v-toolbar-title>
        <v-spacer></v-spacer>
            <!-- <v-avatar>
                <img
                    src="https://cdn.vuetifyjs.com/images/john.jpg"
                    alt="John"
                >
            </v-avatar> -->
            <v-menu
              bottom
              min-width="200px"
              rounded
              offset-y
            >
              <template v-slot:activator="{ on }">
                <v-btn
                  icon
                  x-large
                  v-on="on"
                >
                  <v-avatar
                    >
                    <img
                      src="https://cdn.vuetifyjs.com/images/john.jpg"
                  >
                  </v-avatar>
                </v-btn>
              </template>
              <v-card>
                <v-list-item-content class="justify-center">
                  <div class="mx-auto text-center">
                    <v-avatar size="68"
                      >
                      <img
                        src="https://cdn.vuetifyjs.com/images/john.jpg"
                    >
                    </v-avatar>
                    <h3 class="mt-3 my-1">Kai Yamada</h3>
                    <p class="text-caption mt-1">
                      gpioblink@gmail.com
                    </p>
                    <v-divider class="my-3"></v-divider>
                    <v-btn
                      depressed
                      rounded
                      text
                    >
                      アカウント連携設定
                    </v-btn>
                    <v-divider class="my-3"></v-divider>
                    <v-btn
                      depressed
                      rounded
                      text
                    >
                      ログアウト
                    </v-btn>
                  </div>
                </v-list-item-content>
              </v-card>
            </v-menu>
    </v-toolbar>
</template>
  
  <script lang="ts">
  import Vue from 'vue';
  // import firebase from "firebase";
  
  export default Vue.extend({
    name: 'MainNavBar',
    methods: {
      moveToSearch() {
        if(this.searchQuery) {
          const url = new URL(location.protocol + "//" + location.host + "/app/search/query");
          url.searchParams.set("query", <string>this.searchQuery);
          window.location.href = url.toString();
        }
      }
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
  