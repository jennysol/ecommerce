<template>
  <v-card class="overflow-hidden v-application">
    <v-app-bar
      absolute
      color="white"
      elevate-on-scroll
      scroll-target="#scrolling-techniques-7"
    >
      <div>
        <h2 class="mb-1">Hi, Dwight</h2>
        <div class="row" style="margin-left: 0.03rem">
          <p>1725 Slough Avenue</p>
          <v-icon class="mb-4" color="primary">mdi-chevron-down</v-icon>
        </div>
      </div>
      
      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon color="primary" x-large>mdi-cart-variant</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon color="primary" x-large>mdi-emoticon-outline</v-icon>
      </v-btn>
    </v-app-bar>
    <v-main>
      <v-container>
      </v-container>
    </v-main>
  </v-card>
</template>

<script>
export default {
  name: 'App',
  components: {
  },
  data: () => ({
  }),
};
</script>
<style>
.v-application {
  font-family: 'Lato', sans-serif;
 }
 .theme--light.v-sheet {
   color: #3B3F51 !important;
 }
</style>
