<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <WishCard
        v-for="item in wishlistMock.list"
        :key="item.id"
        :item="item"
        class="mb-5"
      />
    </v-col>
  </v-row>
</template>

<script>
import Logo from '~/components/Logo.vue'
import WishCard from '~/components/WishCard.vue';
import wishlistMock from '~/mocks/wishlist';

export default {
  components: {
    Logo,
    WishCard,
  },

  data() {
    return{ 
      wishlistMock,
    };
  },
}
</script>
