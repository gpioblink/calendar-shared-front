<template>
    <div class="d-flex flex-row">
        <div class="flex-grow-1" align="center"><v-btn icon>
            <v-icon>mdi-radiobox-blank</v-icon>
        </v-btn></div>
        <div class="flex-grow-1" align="center"><v-btn icon>
            <v-icon>mdi-delta</v-icon>
        </v-btn></div>
        <div class="flex-grow-1" align="center"><v-btn icon>
            <v-icon>mdi-close</v-icon>
        </v-btn></div>
        <div class="flex-grow-1" align="center"><v-btn icon>
            <v-icon>mdi-minus</v-icon>
        </v-btn></div>
    </div>
</template>
  
  <script lang="ts">
  import Vue from 'vue';
  // import firebase from "firebase";
  
  export default Vue.extend({
    name: 'CalenderPermissionSelectorItem',
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
        user: { photoURL: "https://bulma.io/images/placeholders/128x128.png"},
        status: 0
      }
    }
  });
  </script>