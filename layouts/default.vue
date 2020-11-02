<template>
  <v-app>
    <Header />

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
import Header from '~/components/Header.vue';

export default {
  name: 'LayoutDefault',

  components: {
    Header,
  },
}
</script>
