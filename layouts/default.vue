<template>
  <v-app >
    <v-app-bar
      :clipped-left="clipped"
      app
      flat
    >
      <!-- <v-app-bar-nav-icon @click.stop="drawer = !drawer" /> -->
      
      <v-toolbar-title class="title" @click="gotoHome">{{ title }}</v-toolbar-title>
      <v-spacer />
      <v-btn text to="/certifications">Certifications</v-btn>
      <v-btn text to="/foodgallery">Food Gallery</v-btn>
      <v-btn text to="/presentations">Presentation</v-btn>
      <v-btn text to="/favoritemenu">Favorite Menu</v-btn>
      <v-btn text to="/about">About Me</v-btn>
      <v-btn
        icon
        @click.stop="rightDrawer = !rightDrawer"
      >
        <v-icon>mdi-menu</v-icon>
      </v-btn>
    </v-app-bar>
    <v-main>
      <!-- <v-container> -->
        <Nuxt />
      <!-- </v-container> -->
    </v-main>
    <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  head() {
      return {
        title: 'Ishant Sharma',
      }
    },
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
      title: 'Ishant'
    }
  },
  methods: {
    gotoHome(){
      $nuxt.$router.push('/')
    }
  }
}
</script>
<style>
body {
        /* font-family: 'Roboto', sans-serif; */
        font-family: 'Libre Baskerville', serif;
        font-weight: bold !important;
}
.heading{
  font-size: 2.5vw;
  font-family: 'Libre Baskerville', serif;
  text-align: center;
}
.title{
  text-transform: uppercase;
  cursor: pointer;
}
</style>