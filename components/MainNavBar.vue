<template>
    <v-toolbar>
        <v-toolbar-title @click="$router.push('/')" style="cursor:pointer">みんなのカレンダー</v-toolbar-title>
        <v-spacer></v-spacer>
            <v-avatar>
                <img
                    src="https://cdn.vuetifyjs.com/images/john.jpg"
                    alt="John"
                >
            </v-avatar>
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
  