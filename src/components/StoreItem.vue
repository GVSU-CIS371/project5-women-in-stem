<template>
  <!-- your answer -->
  <div>
    <v-card>
      <v-card-title>{{ product.data.name }}</v-card-title>
      <v-card-subtitle>{{product.data.rating }}</v-card-subtitle>
      <v-img :src="product.data.image" height="300"></v-img>
      <v-card-text>{{ product.data.description }}</v-card-text>
    </v-card>
  </div>
</template>

<script lang="ts" setup>
// your answer
import { ProductDoc } from '../types/product';

defineProps<{
  product: ProductDoc
}>();
</script>