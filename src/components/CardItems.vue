<template>
  <v-card height="200">
    <v-card-title>{{ props.title }}</v-card-title>
    <v-card-item>{{ props.content }}</v-card-item>
  </v-card>
</template>

<script setup lang="ts">
import { defineComponent } from 'vue';
defineComponent({
  name: 'CardItems',
});
const props = defineProps(['title', 'content']);
</script>
