<template>
  <div>
    <v-card>
      <v-card-title>{{ product.data.name }}</v-card-title>
        <v-row align="center" >  
          <v-rating :model-value="product.data.rating" color="orange-lighten-3" readonly size="16"></v-rating>
          <v-icon icon="mdi-cash" color = "green-lighten-3" class="mr-2" /> {{ product.data.price }}
          <v-icon icon="mdi-package-variant-closed" color = "light-blue-lighten-3" class="mr-2"/>{{ product.data.stock }}
        </v-row>
      <v-spacer></v-spacer>
      <v-img :src="product.data.image" width="200" height="300" class="mx-auto"></v-img>
      <v-card-text>{{ product.data.description }}</v-card-text>
    </v-card>
  </div>
</template>

<script lang="ts" setup>
import { ProductDoc } from '../types/product';

defineProps<{
  product: ProductDoc
}>();
</script>