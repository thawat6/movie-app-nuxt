<template>
  <v-app-bar elevation="0" extension-height="64" color="white">
    <v-spacer />
    <v-toolbar-title>LOGO</v-toolbar-title>
    <v-toolbar-title>
      <v-combobox
        class="mt-5 ml-10"
        dense
        filled
        outlined
        append-icon=""
        prepend-inner-icon="mdi-magnify"
        placeholder="ค้นหา"
      ></v-combobox>
    </v-toolbar-title>
    <v-spacer />
    <v-btn class="mr-2" small> Register </v-btn>
    <v-btn small outlined> Sing in </v-btn>
    <v-spacer />
    <template #extension>
      <v-toolbar color="white">
        <v-container>
          <v-row class="ml-16">
            <h4 class="ml-8" v-for="tag in tagMovies" :key="tag">
              {{ tag }}
            </h4>
          </v-row>
        </v-container>
      </v-toolbar>
    </template>
  </v-app-bar>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      tagMovies: [
        "หนังล่าสุด",
        "แอคชั่น",
        "ซีรี่ส์",
        "การ์ตูน",
        "อนิเมะ",
        "หนังไทย",
        "หนังฝรั่ง",
      ],
    };
  },
};
</script>

<style>
</style>