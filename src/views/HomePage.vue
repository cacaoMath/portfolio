<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <v-hover v-slot="{ isHovering, props }">
          <img
            v-bind="props"
            :src="isHovering ? kubistlogo : logo"
            width="256"
            height="256"
            class="logo"
          />
        </v-hover>
      </v-col>

      <v-col class="mb-4">
        <h1 class="display-2 font-weight-bold mb-3">cacaomath</h1>

        <h4>Vite Preview</h4>

        <p class="subheading font-weight-regular">
          For help and collaboration with other Vuetify developers,
          <br />please join our online
          <a href="https://community.vuetifyjs.com" target="_blank"
            >Discord Community</a
          >
        </p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup lang="ts">
import { defineComponent } from 'vue';

// Logo
import logo from '../assets/cacaomath.svg';
import kubistlogo from '../assets/kubist.svg';

defineComponent({
  name: 'HomePage',

  data() {
    return {
      logo,
      kubistlogo,
    };
  },
});
</script>

<style>
.logo {
  border-radius: 50%;
}
</style>
