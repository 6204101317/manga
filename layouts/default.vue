<template>
  <v-app>
    <v-app-bar :clipped-left="clipped" fixed app>
      <v-switch v-model="$vuetify.theme.dark"></v-switch>
      <v-toolbar-title v-text="title" />
      <v-spacer />
    </v-app-bar>
    <img src="@/layouts/manga.png" />
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer :absolute="!fixed" app> @ jikin Api </v-footer>
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
<style scoped>
.theme--light.v-application {
  background: #c5c0c0;
  color: #020202;
}
.theme--dark.v-application {
  background: #ff7b00;
  color: #020202;
}
v-application .text {
  color: #050505 !important;
  caret-color: #070707 !important;
}
</style>
