<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer">
      <NavigationItem />
    </v-navigation-drawer>

    <v-app-bar>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>cacaomath</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script lang="ts">
import NavigationItem from './components/NavigationItem.vue';
export default {
  components: { NavigationItem },
  data: () => ({ drawer: false }),
};
</script>
