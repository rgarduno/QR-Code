<template>
  <v-app>
    <v-app-bar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>QrCode</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
        <span>rgarduno</span>
    </v-app-bar>

    <v-content>
      <Home />
    </v-content>
  </v-app>
</template>

<script>
import Home from './views/Home.vue';

export default {
  name: 'App',
  components: {
    Home,
  },
  data: () => ({
    //
  }),
};
</script>
