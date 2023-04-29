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
        <div v-for="(media, key) in mediaList" :key="key" class="ma-3">
          <h3>{{ media.name }}</h3>
          <a :href="media.link" target="_blank"
            ><img :src="media.icon" width="30"
          /></a>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup lang="ts">
import { defineComponent } from 'vue';

// Logo
import logo from '../assets/cacaomath.svg';
import kubistlogo from '../assets/kubist.svg';
import githublogo from '../assets/211904_social_github_icon.svg';
import editlogo from '../assets/3994420_draw_edit_new_pen_write_icon.svg';

interface Media {
  name: string;
  icon: string;
  link: string;
}

const mediaList: Array<Media> = [
  {
    name: 'GitHub',
    icon: githublogo,
    link: 'https://github.com/cacaoMath',
  },
  {
    name: 'Qiita',
    icon: editlogo,
    link: 'https://qiita.com/cacaoMath',
  },
];

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
