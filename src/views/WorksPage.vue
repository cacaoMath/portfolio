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
    title: 'RSS collect API',
    subtitle: 'Python, FastAPI',
    content: '指定したRSSの記事から好みの記事を集めるAPI',
    link: 'https://rss-api.cacaomath.com/redoc',
  },
  {
    title: '希望のヒカリ',
    subtitle: 'C#, Unity',
    content:
      '2019/3月に行われた"#Unity1week"というイベントで作ったゲーム。縦スクロールアクションで障害物をよけたりしてスコアを稼いで遊ぶ。',
    link: 'https://unityroom.com/games/kibou-no-hikari',
  },
  {
    title: 'FlowChat',
    subtitle: 'HTML/CSS, JavaScript, Firebase',
    content:
      'ニコニコ動画のようにコメントがブラウザ上で流れてくるアプリ。背景が緑なので透過させてほかの画面に合成もできる。',
    link: 'https://flowchat-7d30c.web.app/index.html',
  },
  {
    title: 'PLACE',
    subtitle: 'Kotlin, Java, Android',
    content:
      'Research"m-Learning時の行動や学習方法が学習効果や安全性に与える影響"で使用した。Androidで英単語学習を行うアプリケーション。フラッシュカード形式や音声で聞き流して学習することができる。',
    link: 'https://github.com/cacaoMath/PLACE#place',
  },
];

defineComponent({
  name: 'WorksPage',
  components: { CardItems },
});
</script>
