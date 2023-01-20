<template>
  <q-layout view="lHh lpR lFr">
    <q-banner inline-actions class="text-white bg-red" style="margin-top: 50px">
      Le site est en cours de construction.
    </q-banner>
    <q-header elevated>
      <q-toolbar class="bg-myBlue text-white shadow-2">
        <q-btn flat label="Thomas Denecker, PhD" />
        <q-space />
        <q-tabs v-model="tab" shrink>
          <q-tab name="tab1" label="Tab 1" />
          <q-tab name="tab2" label="Tab 2" />
          <q-tab name="tab3" label="Tab 3" />
        </q-tabs>
      </q-toolbar>
    </q-header>

    <div class="row justify-between" >
      <q-parallax src="img/banner.png"> </q-parallax>
    </div>

    <div align="center">
      <q-card class="my-card" flat>
        <q-card-section horizontal>
          <q-img
            class="col-5"
            src="http://thomas.denecker.free.fr/assets/img/profile.jpg"
          />
          <q-card-section class="q-ma-lg text-left">
            <p class="text-h4">Thomas Denecker, PhD</p>
            <p class="text-subtitle1 myBlue">
              <b>Research engineer - Open Science</b><br />
              Institut Français de Bioinformatique
            </p>
            <p><b>Adress</b> <br />15 Rue Traversière,<br />75012 Paris</p>
          </q-card-section>
        </q-card-section>
        <q-card-actions class="bg-myBlue text-white" align="center">
          <q-btn
            flat
            :icon="iconGithub"
            href="https://github.com/thomasdenecker"
            target="_blank"
          />
          <q-btn
            flat
            :icon="iconGitlab"
            href="https://gitlab.com/thomasdenecker"
            target="_blank"
          />
          <q-btn
            flat
            :icon="iconLinkedin"
            href="https://www.linkedin.com/in/thomas-denecker/"
            target="_blank"
          />
        </q-card-actions>
      </q-card>
    </div>

    <q-page-container>
      <div class="q-px-lg q-pt-sm">
        <router-view />
      </div>
    </q-page-container>

    <q-footer elevated class="bg-grey-8 text-white">
      <div class="text-center">Thomas Denecker, PhD - © 2023</div>
    </q-footer>
  </q-layout>
</template>

<script>
import { ref } from "vue";
import { mdiGithub, mdiGitlab, mdiLinkedin } from "@quasar/extras/mdi-v7";

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
  created() {
    this.iconGithub = mdiGithub;
    this.iconGitlab = mdiGitlab;
    this.iconLinkedin = mdiLinkedin;
  },
};
</script>

<style lang="scss" scoped>
h2,
h3,
h4 {
  color: $myBlue;
}

h2::after {
  content: "";
  display: block;
  width: 300px;
  height: 3px;
  background: $mylightBlue !important;
  margin-top: 3px;
  box-sizing: border-box;
}
.bg-myBlue {
  background: $myBlue !important;
}

.myBlue {
  color: $myBlue !important;
}
.my-card {
  width: 100%;
  max-width: 800px;
  position: relative;
  margin: -300px 0px -50px 0px;
}
</style>