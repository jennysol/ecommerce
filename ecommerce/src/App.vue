<template>
  <v-card class="overflow-hidden v-application">
    <app-bar/>
    <v-main>
      <v-container>
      </v-container>
    </v-main>
  </v-card>
</template>

<script>
import AppBar from './components/layouts/AppBar'
export default {
  name: 'App',
  components: {
    AppBar
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
  .title {
      font-size: 22px;
  }
  .subtitle {
    font-size: 14px;
  }
</style>
