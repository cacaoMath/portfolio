<template>
  <v-list nav dense>
    <v-list-item v-for="(item, key) in nav_list" :key="key">
      <v-list-item-content>
        <v-list-item-title class="title"> {{ item.name }} </v-list-item-title>
      </v-list-item-content>
    </v-list-item>
  </v-list>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

interface NavItem {
  name: string;
  link: string;
}
const home: NavItem = { name: 'home', link: '' };
const about: NavItem = { name: 'about', link: '' };
const work: NavItem = { name: 'work', link: '' };
export default defineComponent({
  name: 'NavigationItem',

  data() {
    return {
      nav_list: [home, about, work] as Array<NavItem>,
    };
  },
});
</script>
