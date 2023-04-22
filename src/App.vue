<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer">
      <!--  -->
    </v-navigation-drawer>

    <v-app-bar>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>cacaomath</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <BioItem></BioItem>
    </v-main>
  </v-app>
</template>

<script lang="ts">
import BioItem from './components/BioItem.vue';
export default {
  components: { BioItem },
  data: () => ({ drawer: false }),
};
</script>
