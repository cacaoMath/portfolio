<!-- カードコンテナ、カードのリストから、リストの要素数分カードを作る -->
<template>
  <v-container>
    <v-row>
      <v-col
        v-for="(item, key) in props.itemList"
        :key="key"
        cols="4"
        align-self="center"
      >
        <v-card
          :title="item.title"
          :subtitle="item.subtitle"
          :text="item.content"
          variant="tonal"
        />
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup lang="ts">
import { defineComponent } from 'vue';

export interface CardItem {
  title: string;
  subtitle: string;
  content: string;
}

defineComponent({
  name: 'CardItems',
});

const props = defineProps({
  itemList: Array<CardItem>,
});
</script>
