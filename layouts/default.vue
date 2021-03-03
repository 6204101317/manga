<template>
  <v-app>
    <v-app-bar :clipped-left="clipped" fixed app>
      <v-switch v-model="$vuetify.theme.dark"></v-switch>
      <v-toolbar-title v-text="title" />
      <v-spacer />
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer :absolute="!fixed" app>
      @ jikin Api
      <!-- <span>&copy; {{ new Date().getFullYear() }}</span> -->
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      fixed: false,

      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Manga!!!!!!',
    }
  },
}
</script>
