<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="10" md="8" lg="6">
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
import WishCard from '~/components/WishCard.vue';
import wishlistMock from '~/mocks/wishlist';

export default {
  components: {
    WishCard,
  },

  data() {
    return{ 
      wishlistMock,
    };
  },
}
</script>
