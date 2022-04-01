<template>
  <v-col cols="12">
    <v-sheet
      class="mx-auto"
    >
      <v-slide-group multiple>
        <v-slide-item
          v-for="product in featuredProducts"
          :key="product.id"
        >
          <v-card height="50%" width="70%" flat>
            <div class="d-flex flex-no-wrap justify-space-between">
              <v-avatar
                class="ma-3"
                tile
              >
                <v-img :src="product.image"></v-img>
              </v-avatar>
              <div >
                <v-card-title class="title">${{ product.price }}</v-card-title>
                <v-card-subtitle class="subtitle">{{ product.title }}</v-card-subtitle>
                <v-btn color="primary" small>Adicionar</v-btn>
              </div>
            </div>
          </v-card>
        </v-slide-item>
      </v-slide-group>
    </v-sheet>
  </v-col>
</template>

<script>
  export default {
    name: 'FeaturedProducts',
    data: () => ({
      featuredProducts: [],
      model: null
    }),
    mounted() {
      this.getFeaturedProducts()
    },
    methods: {
      getFeaturedProducts() {
        fetch('https://fakestoreapi.com/products?limit=5')
          .then(res=> res.json())
          .then(json=> this.featuredProducts = json)
      }
    }
  }
</script>
