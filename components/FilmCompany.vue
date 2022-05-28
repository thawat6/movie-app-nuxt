<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="8">
      <h2 class="text-center">ค่ายหนัง</h2>
      <v-sheet class="mx-auto" elevation="0" max-width="800">
        <v-slide-group v-model="model" class="pa-4" center-active show-arrows>
          <v-slide-item
            v-for="card in cards"
            :key="card.title"
            v-slot="{ active, toggle }"
          >
            <v-card
              :color="active ? 'primary' : 'grey lighten-1'"
              class="ma-4 mr-0"
              height="100"
              width="140"
              outline
              @click="toggle"
            >
              <v-row class="fill-height" align="center" justify="center">
                <v-scale-transition>
                  <h3 class="pt-6" v-text="card.title"></h3>
                </v-scale-transition>
              </v-row>
            </v-card>
          </v-slide-item>
        </v-slide-group>
      </v-sheet>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data: () => ({
    model: null,
    cards: [
      {
        title: "MARVEL",
        src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
        flex: 3,
        height: 100,
      },
      {
        title: "DC",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 3,
        height: 100,
      },
      {
        title: "FOX",
        src: "https://cdn.vuetifyjs.com/images/cards/house.jpg",
        flex: 3,
        height: 100,
      },
      {
        title: "PARAMOUNT",
        src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
        flex: 3,
        height: 100,
      },
      {
        title: "บั้งไฟ",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 3,
        height: 100,
      },
      {
        title: "LION",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 3,
        height: 100,
      },
    ],
  }),
};
</script>

<style lang="scss" scoped>
.v-card__title {
  font-weight: 700;
  flex-direction: column-reverse;
}
</style>

