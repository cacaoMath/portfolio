<template>
  <CardItems :item-list="journalCardItems" />

  <CardItems :item-list="programmingCardItems" />
</template>

<script setup lang="ts">
import { defineComponent } from 'vue';
import CardItems, { CardItem } from '../components/CardItems.vue';

const journalCardItems: Array<CardItem> = [
  {
    title: 'a',
    content: 'none',
  },
  {
    title: 'b',
    content: 'none',
  },
  {
    title: 'a',
    content: 'none',
  },
  {
    title: 'b',
    content: 'none',
  },
];

const programmingCardItems: Array<CardItem> = [
  {
    title: 'a',
    content: 'none',
  },
  {
    title: 'b',
    content: 'none',
  },
  {
    title: 'a',
    content: 'none',
  },
  {
    title: 'b',
    content: 'none',
  },
];

defineComponent({
  name: 'WorksPage',
  components: { CardItems },
});
</script>
