<template>
  <q-banner inline-actions class="text-white bg-red">
    Le site est en cours de construction.
  </q-banner>
  <q-layout view="lHh lpR lFr">
    <q-drawer show-if-above v-model="leftDrawerOpen" side="left" bordered>
      <div class="text-center q-pt-sm">
        <q-avatar size="125px">
          <img src="http://thomas.denecker.free.fr/assets/img/profile.jpg" />
        </q-avatar>
        <p class="text-h5">
          Thomas Denecker <br />
          PhD
        </p>
        <p class="text-overline">Research engineer</p>
      </div>
    </q-drawer>

    <q-page-container>
      <div class="q-px-lg q-pt-sm">
        <router-view />
      </div>
    </q-page-container>

    <q-footer elevated class="bg-grey-8 text-white">
      <q-toolbar>
        <q-toolbar-title>
          <div>Thomas Denecker - © 2023</div>
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>
  </q-layout>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const leftDrawerOpen = ref(false);

    return {
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
};
</script>