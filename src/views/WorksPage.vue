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
    subtitle: 'string',
    content: 'none',
  },
  {
    title: 'b',
    subtitle: 'string',
    content: 'none',
  },
  {
    title: 'a',
    subtitle: 'string',
    content: 'none',
  },
  {
    title: 'b',
    subtitle: 'string',
    content: 'none',
  },
];

const programmingCardItems: Array<CardItem> = [
  {
    title: 'a',
    subtitle: 'string',
    content: 'none',
  },
  {
    title: 'b',
    subtitle: 'string',
    content: 'none',
  },
  {
    title: 'a',
    subtitle: 'string',
    content: 'none',
  },
  {
    title: 'b',
    subtitle: 'string',
    content: 'none',
  },
];

defineComponent({
  name: 'WorksPage',
  components: { CardItems },
});
</script>
