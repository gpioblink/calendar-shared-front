<template>
  <v-app :style="{ background: '#F5F5F5' }">
    <v-main>
      <RoomNavBar />

      <v-container class="spacing-playground pa-6">
        <Nuxt/>
      </v-container>
    </v-main>
    <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }} Zli Team Happy BirthDay</span>
    </v-footer>
  </v-app>
</template>
  
  <script>
  export default {
    name: 'AppLayout',
    data () {
      return {
        clipped: false,
        drawer: false,
        fixed: false,
        items: [
          {
            icon: 'mdi-apps',
            title: 'Welcome',
            to: '/'
          },
          {
            icon: 'mdi-chart-bubble',
            title: 'Inspire',
            to: '/inspire'
          }
        ],
        miniVariant: false,
        right: true,
        rightDrawer: false,
        title: 'Vuetify.js'
      }
    }
  }
  </script>
  