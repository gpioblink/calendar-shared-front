<template>
    <v-list-item>
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
    },
    data() {
      return {
      }
    }
  });
  </script>