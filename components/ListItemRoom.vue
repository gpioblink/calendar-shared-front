<template>
    <v-list-item link to="/room"
    >
        <v-list-item-avatar>
        <v-icon
            class="grey lighten-1"
            dark
        >
        mdi-cat
        </v-icon>
        </v-list-item-avatar>

        <v-list-item-content>
            <v-list-item-title>Zliルーム</v-list-item-title>
        </v-list-item-content>

        <v-list-item-action>
            <v-btn icon><v-icon>mdi-calendar-plus</v-icon></v-btn>
        </v-list-item-action>
    </v-list-item>
</template>
  
  <script lang="ts">
  import Vue from 'vue';
  // import firebase from "firebase";
  
  export default Vue.extend({
    name: 'ListItemRoom',
    methods: {
    },
    mounted() {
    },
    data() {
      return {
      }
    }
  });
  </script>