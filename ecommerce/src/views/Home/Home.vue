<template>
  <v-col cols="12" class="mt-6">
    <v-row>
      <v-col cols="12">
        <v-text-field 
          v-model="search" 
          solo 
          placeholder="Busque seu produto"
        >
          <v-icon
            slot="append"
            color="primary"
          >
            mdi-magnify
          </v-icon>
        </v-text-field>
      </v-col>
      <FeaturedProducts/>
    </v-row>
  </v-col>
</template>

<script>
import FeaturedProducts from '../../components/FeaturedProducts'
export default {
  name: 'Home',
  components: { FeaturedProducts },
  data: () => ({
      search: '',
  }),
}
</script>
