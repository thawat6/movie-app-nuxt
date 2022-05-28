<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="8">
      <h2 class="text-center">หมวดหมู่</h2>
      <v-container fluid>
        <v-row dense>
          <v-col class="pt-0 pr-3" cols="3">
            <v-card>
              <v-img
                src="https://cdn.vuetifyjs.com/images/cards/road.jpg"
                class="mt-0 white--text align-center"
                gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                height="220"
              >
                <v-card-title v-text="`หนังล่าสุด`"></v-card-title>
              </v-img>
            </v-card>
          </v-col>
          <v-col class="pa-0" cols="9">
            <v-row>
              <v-col v-for="card in cards" :key="card.title" cols="4">
                <v-card>
                  <v-img
                    :src="card.src"
                    class="white--text align-center"
                    gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                    :height="card.height"
                  >
                    <v-card-title v-text="card.title"></v-card-title>
                  </v-img>
                </v-card>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data: () => ({
    cards: [
      {
        title: "แอคชั่น",
        src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
        flex: 3,
        height: 100,
      },
      {
        title: "การ์ตูน",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 3,
        height: 100,
      },
      {
        title: "หนังฝรั่ง",
        src: "https://cdn.vuetifyjs.com/images/cards/house.jpg",
        flex: 3,
        height: 100,
      },
      {
        title: "ซีรี่ส์",
        src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
        flex: 3,
        height: 100,
      },
      {
        title: "อนิเมะ",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 3,
        height: 100,
      },
      {
        title: "หนังไทย",
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

