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
    link: 'https://cacaomath.com',
  },
  {
    title: 'b',
    subtitle: 'string',
    content: 'none',
    link: 'https://cacaomath.com',
  },
  {
    title: 'a',
    subtitle: 'string',
    content: 'none',
    link: 'https://cacaomath.com',
  },
  {
    title: 'b',
    subtitle: 'string',
    content: 'none',
    link: 'https://cacaomath.com',
  },
];

const programmingCardItems: Array<CardItem> = [
  {
    title: 'a',
    subtitle: 'string',
    content: 'none',
    link: 'https://cacaomath.com',
  },
  {
    title: 'b',
    subtitle: 'string',
    content: 'none',
    link: 'https://cacaomath.com',
  },
  {
    title: 'a',
    subtitle: 'string',
    content: 'none',
    link: 'https://cacaomath.com',
  },
  {
    title: 'b',
    subtitle: 'string',
    content: 'none',
    link: 'https://cacaomath.com',
  },
];

defineComponent({
  name: 'WorksPage',
  components: { CardItems },
});
</script>
