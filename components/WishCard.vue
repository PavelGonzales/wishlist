<template>
  <v-card class="rounded-lg elevation-1">
    <div class="d-flex flex-no-wrap">
      <div class="mt-5 ml-5">
        <v-avatar
          size="125"
          tile
        >
          <v-img contain :src="item.image" />
        </v-avatar>
          <v-rating
            :value="item.rating"
            color="amber"
            dense
            half-increments
            readonly
            size="14"
            class="mb-2"
          />

          <div class="caption text--disabled">Цена</div>
          <div class="subtitle-1 mb-3">
            {{ priceString }}
          </div>

          <v-btn
            v-if="item.url"
            :href="item.url"
            target="_blank"
            class="elevation-0 mb-4"
            color="success"
            outlined
          >
            Подарить
          </v-btn>
      </div>
    

      <div>
        <v-card-title class="headline">
          <div class="caption text--disabled w-100">Название</div>
          {{ item.title }}
        </v-card-title>
        <v-card-subtitle v-if="item.description" class="pt-3">
          <div class="caption text--disabled w-100">Описание</div>
          {{ item.description }}
        </v-card-subtitle>
      </div>
    </div>
  </v-card>
</template>

<script>
export default {
  name: 'WishCard',

  props: {
    item: {
      type: Object,
      required: true,
    },
  },

  computed: {
    priceString() {
      const stringArr = [];
      const priceRange = this.item.priceRange || {};

      if (priceRange.start) {
        stringArr.push(`${priceRange.start}₽`)
      }
      if (priceRange.start && priceRange.end) {
        stringArr.push('–')
      }
      if (priceRange.end) {
        stringArr.push(`${priceRange.end}₽`)
      }
      return stringArr.join(' ')
    },
  },
}
</script>

<style scoped>
.v-card__title {
  word-break: initial;
}

.w-100 {
  width: 100%;
}
</style>
