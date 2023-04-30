<!-- カードコンテナ、カードのリストから、リストの要素数分カードを作る -->
<template>
  <v-container>
    <v-row>
      <v-col
        v-for="(item, key) in props.itemList"
        :key="key"
        cols="5"
        align-self="center"
      >
        <v-hover v-slot="{ isHovering, props }">
          <v-card
            variant="tonal"
            height="200"
            max-height="300"
            :elevation="isHovering ? 10 : 2"
            v-bind="props"
            :href="item.link"
            target="_blank"
          >
            <div class="bg-surface-variant pb-2">
              <v-card-title class="text-h5 flex-column text-truncate text-lg">{{
                item.title
              }}</v-card-title>
              <v-card-subtitle>{{ item.subtitle }}</v-card-subtitle>
            </div>
            <v-card-text>{{ item.content }}</v-card-text>
          </v-card>
        </v-hover>
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
  link: string;
}

defineComponent({
  name: 'CardItems',
});

const props = defineProps({
  itemList: Array<CardItem>,
});
</script>
