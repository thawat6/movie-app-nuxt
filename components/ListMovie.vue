<template>
  <div>
    <v-row>
      <v-col class="text-left" cols="2" sm="2" md="2">
        <h3>ปีที่ฉาย</h3>
        <v-row class="pt-5 pb-5">
          <v-btn text v-for="year in years" :key="year">
            {{ year }}
          </v-btn>
        </v-row>
        <h3>หมวดหมู่</h3>
        <v-row class="pt-5 pb-5">
          <v-btn
            text
            block
            v-for="category in categories"
            :key="'category' + category"
          >
            <li>{{ category }}</li>
          </v-btn>
        </v-row>
        <h3>ประเภท</h3>
        <v-row class="pt-5">
          <v-btn text block v-for="type in types" :key="'type' + type">
            <li>{{ type }}</li>
          </v-btn>
        </v-row>
      </v-col>
      <v-col cols="8" sm="8" md="8">
        <v-row>
          <h3 class="pa-3 pl-0" v-for="tag in mainTags" :key="'tag' + tag">
            {{ tag }} |
          </h3>
        </v-row>
        <v-row>
          <v-col
            v-for="(card, i) in cards"
            :key="'title' + i"
            :cols="card.flex"
          >
            <v-card>
              <v-img
                :src="card.src"
                class="white--text align-end"
                gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                :height="card.height"
              >
                <v-card-subtitle v-text="card.title"></v-card-subtitle>
              </v-img>
            </v-card>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
    <div class="pt-8 text-center">
      <v-pagination v-model="page" :length="6"></v-pagination>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    types: [
      "Biography ชีวประวัติ",
      "Adventure ผจญภัย",
      "Action แอคชั่น",
      "Comedy ตลก",
      "History ประวัติศาสตร์",
      "Western ตะวันตก",
      "War สงคราม",
      "Thriller ระทึกขวัญ",
      "Sci-fi วิทยาศาสตร์",
      "Romance โรแมนติก",
      "Mystery ลึกลับ",
      "Musical ดนตรี",
      "Fantasy แฟนตาซี",
      "Family ครอบครัว",
      "Drama ชีวิต",
      "Documentary สารคดี",
      "Crime อาชญากรรม",
    ],
    categories: [
      "หมวดหมู",
      "หนังซูม",
      "หนังฝรั่ง",
      "หนังไทย",
      "ซีรี่ส์",
      "การ์ตูน",
      "อนิเมะ",
    ],
    page: 1,
    model: null,
    mainTags: ["อัพเดตล่าสุด", "หนังเรียงตามปี", "TOP IMDM", "คนชอบมากที่สุด"],
    cards: [
      {
        title: "MARVEL",
        src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
        flex: 3,
        height: 250,
      },
      {
        title: "DC",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 3,
        height: 250,
      },
      {
        title: "FOX",
        src: "https://cdn.vuetifyjs.com/images/cards/house.jpg",
        flex: 3,
        height: 250,
      },
      {
        title: "PARAMOUNT",
        src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
        flex: 3,
        height: 250,
      },
      {
        title: "บั้งไฟ",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 3,
        height: 250,
      },
      {
        title: "LION",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 3,
        height: 250,
      },
      {
        title: "MARVEL",
        src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
        flex: 3,
        height: 250,
      },
      {
        title: "DC",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 3,
        height: 250,
      },
      {
        title: "FOX",
        src: "https://cdn.vuetifyjs.com/images/cards/house.jpg",
        flex: 3,
        height: 250,
      },
      {
        title: "PARAMOUNT",
        src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
        flex: 3,
        height: 250,
      },
      {
        title: "บั้งไฟ",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 3,
        height: 250,
      },
      {
        title: "LION",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 3,
        height: 250,
      },
      {
        title: "FOX",
        src: "https://cdn.vuetifyjs.com/images/cards/house.jpg",
        flex: 3,
        height: 250,
      },
      {
        title: "PARAMOUNT",
        src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
        flex: 3,
        height: 250,
      },
      {
        title: "บั้งไฟ",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 3,
        height: 250,
      },
      {
        title: "LION",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 3,
        height: 250,
      },
      {
        title: "FOX",
        src: "https://cdn.vuetifyjs.com/images/cards/house.jpg",
        flex: 3,
        height: 250,
      },
      {
        title: "PARAMOUNT",
        src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
        flex: 3,
        height: 250,
      },
      {
        title: "บั้งไฟ",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 3,
        height: 250,
      },
      {
        title: "LION",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 3,
        height: 250,
      },
    ],
  }),
  computed: {
    years() {
      var start_year = new Date().getFullYear();
      var year = [];
      for (var i = start_year; i > start_year - 20; i--) {
        year.push(i);
      }
      return year;
    },
  },
};
</script>

<style lang="scss" scoped>
.v-btn {
  justify-content: flex-start;
}
</style>

