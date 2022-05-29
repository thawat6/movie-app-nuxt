<template>
  <div>
    <v-card
      v-if="adsBottom"
      dark
      class="mx-auto sticky-card-bottom-first"
      max-width="750"
      color="primary"
    >
      <v-card-text>
        <v-btn
          style="top: 0px; right: 0px"
          color="pink"
          small
          dark
          absolute
          top
          right
          @click="adsBottom = false"
        >
          ปิด<v-icon>mdi-close</v-icon>
        </v-btn>

        <div class="text-center">Ads</div>
      </v-card-text>
    </v-card>
    <v-card
      v-if="adsBottom"
      dark
      class="mx-auto sticky-card-bottom-second"
      max-width="750"
      color="primary"
    >
      <v-card-text>
        <v-btn
          style="top: 0px; right: 0px"
          color="pink"
          small
          dark
          absolute
          top
          right
          @click="adsBottom = false"
        >
          ปิด<v-icon>mdi-close</v-icon>
        </v-btn>

        <div class="text-center">Ads</div>
      </v-card-text>
    </v-card>
    <v-card
      v-if="adsSide"
      dark
      class="mx-auto sticky-card-bottom-left"
      max-width="200"
      color="primary"
    >
      <v-card-text>
        <v-btn
          fab
          style="top: 0px; right: 0px"
          color="pink"
          dark
          absolute
          top
          right
          x-small
          @click="adsSide = false"
        >
          <v-icon>mdi-close</v-icon>
        </v-btn>

        <div class="text-center">Ads</div>
      </v-card-text>
    </v-card>
    <v-card
      v-if="adsSide"
      dark
      class="mx-auto sticky-card-bottom-right"
      max-width="200"
      color="primary"
    >
      <v-card-text>
        <v-btn
          fab
          style="top: 0px; left: 0px"
          color="pink"
          dark
          absolute
          top
          left
          x-small
          @click="adsSide = false"
        >
          <v-icon>mdi-close</v-icon>
        </v-btn>

        <div class="text-center">Ads</div>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      adsSide: true,
      adsBottom: true,
    };
  },
};
</script>

<style lang="scss" scoped>
.sticky-card-bottom-first {
  width: 50%;
  position: fixed;
  bottom: 65px;
  z-index: 1;
  padding-bottom: 20px;
  padding-top: 20px;

  left: 50%;
  transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  -webkit-transform: translate(-50%, -50%);
}
.sticky-card-bottom-second {
  width: 50%;
  position: fixed;
  bottom: 0;
  z-index: 1;
  padding-bottom: 20px;
  padding-top: 20px;

  left: 50%;
  transform: translate(-50%, -10%);
  -ms-transform: translate(-50%, -10%);
  -webkit-transform: translate(-50%, -10%);
}
.sticky-card-bottom-left {
  width: 50%;
  position: fixed;
  top: 140px;
  z-index: 1;
  padding-bottom: 250px;
  padding-top: 250px;
}
.sticky-card-bottom-right {
  width: 50%;
  position: fixed;
  top: 140px;
  z-index: 1;
  padding-bottom: 250px;
  padding-top: 250px;
  right: 0;
}
</style>