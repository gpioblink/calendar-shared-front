<template>
    <v-list-item>
        <!-- <v-list-item-title>ほげほげカレンダー</v-list-item-title> -->
        <v-list-item-content>
            <v-row align="center" justify="center">
                <v-col col="6">
                    <v-list-item-title>ほげほげカレンダー</v-list-item-title>
                </v-col>
                <v-col col="6">
                    <div>
                        <ButtonStatus></ButtonStatus>
                        <ButtonPermission></ButtonPermission>
                    </div>
                </v-col>
            </v-row>
        </v-list-item-content>
        
        <!-- <v-list-item-action-text>あああああああ</v-list-item-action-text> -->
    </v-list-item>
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