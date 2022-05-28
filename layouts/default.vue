<template>
  <v-app dark>
    <AppBar />
    <Ads />
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>

    <v-footer :absolute="!fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "DefaultLayout",
  data() {
    return {
      fixed: false,
    };
  },
};
</script>
<style lang="scss">
.v-btn__content {
  text-transform: none !important;
}
.v-toolbar__content,
.v-toolbar__extension {
  padding: 0;
}
</style>