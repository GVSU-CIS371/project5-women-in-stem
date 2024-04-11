<template>
  <!-- your answer -->
  <div>
    <v-card>
      <v-card-title>{{ props.product.data.name }}</v-card-title>
      <v-card-subtitle>{{props.product.data.rating }}</v-card-subtitle>
      <v-img :src="props.product.data.image" height="300"></v-img>
      <v-card-text>{{ props.product.data.description }}</v-card-text>
    </v-card>
  </div>
</template>

<script lang="ts" setup>
// your answer
import { defineProps } from 'vue';
import { ProductDoc } from '../types/product';

const props = defineProps({
  product: {
    type: Object as () => ProductDoc,
    required: true
  }
});
</script>