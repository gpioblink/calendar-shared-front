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