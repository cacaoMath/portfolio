<template>
  <v-container>
    <h2>Research</h2>
    <CardItems :item-list="journalCardItems" />

    <h2>Programming</h2>
    <CardItems :item-list="programmingCardItems" />
  </v-container>
</template>

<script setup lang="ts">
import { defineComponent } from 'vue';
import CardItems, { CardItem } from '../components/CardItems.vue';

const journalCardItems: Array<CardItem> = [
  {
    title:
      'Feature Analysis to Estimate Sleep Time Based on Simple Measurement of Biological Information after Awakening',
    subtitle:
      'Mahiro Imabeppu, Ren Katsurada, Tatsuhito Hasegawa; IJBBB; Jul. 2020',
    content:
      'Keyword: Wearable device, Sleep time estimation, Support vector machine, Electrooculogram.',
    link: 'http://www.ijbbb.org/show-85-939-1.html',
  },
  {
    title:
      'Effects of Different Activities on Learning Efficiency of m-Learning Users',
    subtitle:
      'Mahiro Imabeppu, 2021 IEEE TALE Tatsuhito Hasegawa; December. 2021',
    content:
      'Keywords: m-Learning, Learning Efficiency, Confidence Rating, Activity Recognition',
    link: 'https://ieeexplore.ieee.org/document/9678604',
  },
  {
    title: 'm-Learning時の行動や学習方法が学習効果や安全性に与える影響',
    subtitle: '今別府 万大, 長谷川 達人; 情報処理学会論文誌; 2022/12/15',
    content: 'Keyword: m-Learning, 歩きスマホ, 学習効果',
    link: 'https://cir.nii.ac.jp/crid/1390575960085275392',
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
