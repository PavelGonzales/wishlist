<template>
  <v-app-bar
    class="rounded-b-xl px-3"
    color="white"
    app
    elevate-on-scroll
    fixed
  >
    <v-spacer />
    <v-toolbar-title>{{ title }}</v-toolbar-title>
    <v-spacer />

    <v-menu
      class="rounded-lg"
      content-class="rounded-lg elevation-1"
      offset-y
    >
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          icon
          color="purple"
          dark
          v-bind="attrs"
          v-on="on"
        >
          <v-avatar
            size="36"
          >
            <img
              src="https://scontent.fhel3-1.fna.fbcdn.net/v/t1.0-9/75231871_1139264909603819_3068452561863311360_n.jpg?_nc_cat=101&ccb=2&_nc_sid=09cbfe&_nc_ohc=Q5tDjtVY4VMAX9Iczy5&_nc_ht=scontent.fhel3-1.fna&oh=fa35b01b06fa4ff312b78a13083a2a8d&oe=5FC7A65A"
              alt="Pavel Gonzales"
            >
          </v-avatar>
        </v-btn>
      </template>
      <v-list min-width="180">
        <v-list-item to="/" color="purple">
          <v-list-item-title>Вишлист</v-list-item-title>
        </v-list-item>
        <v-list-item to="/profile" color="purple">
          <v-list-item-title>Профиль</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </v-app-bar>
</template>

<script>
export default {
  name: 'Header',

  computed: {
    title() {
      return this.$route.name;
    },
  },
}
</script>
