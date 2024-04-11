<template>
  <div>
    <v-card>
      <v-card-title>{{ product.data.name }}</v-card-title>
      <v-row>
            
            <v-rating :model-value="product.data.rating" color="yellow-darken-1" readonly></v-rating>
            <v-icon icon="mdi-cash" /> {{ product.data.price }}
            <v-icon icon="mdi-package-variant-closed" />{{ product.data.stock }}
          </v-row>
      <v-img :src="product.data.image" height="300"></v-img>
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