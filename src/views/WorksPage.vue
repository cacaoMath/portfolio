<template>
  <v-container>
    a
    <v-row>
      <v-col
        v-for="(item, key) in programmingCardItems"
        :key="key"
        cols="4"
        align-self="center"
      >
        <CardItems :title="item.title" :content="item.content" />
      </v-col>
    </v-row>
  </v-container>
  <v-container>
    a
    <v-row>
      <v-col
        v-for="(item, key) in journalCardItems"
        :key="key"
        cols="4"
        align-self="center"
      >
        <CardItems :title="item.title" :content="item.content" />
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup lang="ts">
import { Ref, defineComponent, ref } from 'vue';
import CardItems from '../components/CardItems.vue';

interface CardItem {
  title: string;
  content: string;
}
const journalCardItems: Ref<Array<CardItem>> = ref([
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
]);

const programmingCardItems: Ref<Array<CardItem>> = ref([
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
]);
defineComponent({
  name: 'WorksPage',
  components: { CardItems },
});
</script>
