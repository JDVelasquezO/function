<template>
  <v-app>
    <v-app-bar app color='indigo darken-1' class="white--text">
      <v-toolbar-title class="headline text-uppercase">
        <span>FUNCT</span>
        <span class="font-weight-light">ION</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        text
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
      >
        <!-- <span class="mr-2">Latest Release</span> -->
      </v-btn>
    </v-app-bar>

    <v-content>
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',
  components: {
    HelloWorld,
  },
  data: () => ({
    //
  }),
};
</script>
