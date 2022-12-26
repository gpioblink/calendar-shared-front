<template>
    <v-btn-toggle class="d-flex flex-row">
        <v-btn text x-small class="flex-grow-1">
            内容も公開
        </v-btn>
        <v-btn x-small class="flex-grow-1">
            有無のみ
        </v-btn>
    </v-btn-toggle>
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
        user: { photoURL: "https://bulma.io/images/placeholders/128x128.png"}
      }
    }
  });
  </script>