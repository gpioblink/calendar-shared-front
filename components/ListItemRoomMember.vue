<template>
    <v-list-item
    >
        <v-list-item-avatar>
            <v-icon
            class="grey lighten-1"
            dark
            >
            mdi-account
            </v-icon>
        </v-list-item-avatar>

        <v-list-item-content>
            <v-list-item-title>じぶりん</v-list-item-title>
        </v-list-item-content>

        <v-list-item-action>
            <v-btn icon><v-icon>mdi-cancel</v-icon></v-btn>
        </v-list-item-action>
    </v-list-item>
</template>
  
  <script lang="ts">
  import Vue from 'vue';
  // import firebase from "firebase";
  
  export default Vue.extend({
    name: 'ListItemRoomMember',
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