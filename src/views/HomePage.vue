<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <v-hover v-slot="{ isHovering, props }">
          <v-img
            v-bind="props"
            :src="isHovering ? kubistlogo : logo"
            height="200"
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

<script lang="ts">
import { defineComponent } from 'vue';

// Logo
import logo from '../assets/cacaomath.svg';
import kubistlogo from '../assets/kubist.svg';

export default defineComponent({
  name: 'HomePage',

  data() {
    return {
      logo,
      kubistlogo,
    };
  },
});
</script>
