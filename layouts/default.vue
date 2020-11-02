<template>
  <v-app>
    <v-app-bar
      fixed
      app
    >
      <v-toolbar-title>{{ title }}</v-toolbar-title>
      <v-spacer />
      <v-btn
        icon
      >
        <v-icon>mdi-menu</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>

    <v-footer app class="justify-center">
      Вишлист &copy; {{ new Date().getFullYear() }}
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      title: 'Pavel Gonzales WishList'
    }
  }
}
</script>
