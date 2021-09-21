<template>
  <q-layout view="lHr lpR fFf">
    <q-header bordered class="bg-white text-black">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="toggleLeftDrawer" />

        <q-toolbar-title class="text-h6 text-weight-bold">
          Fake Twitter
        </q-toolbar-title>
      </q-toolbar>
    </q-header>
    <!--qqq qqq qqq patriots are in control now... -->
    <q-drawer
      :width="283"
      show-if-above
      v-model="leftDrawerOpen"
      side="left"
      bordered
    >
      <q-icon class="q-pa-md" name="style" size="lg" color="primary" />
      <q-list bordered>
        <q-item to="/" clickable v-ripple>
          <q-item-section avatar>
            <q-icon name="home" />
          </q-item-section>

          <q-item-section class="text-h6 text-weight-bold">Home</q-item-section>
        </q-item>
        <q-item to="/about" clickable v-ripple>
          <q-item-section avatar>
            <q-icon name="help" />
          </q-item-section>

          <q-item-section class="text-h6 text-weight-bold"
            >About</q-item-section
          >
        </q-item>
      </q-list>
    </q-drawer>

    <q-drawer show-if-above v-model="rightDrawerOpen" side="right" bordered>
      <q-input
        class="q-ma-md"
        outlined
        rounded
        placeholder="Search Fake Twitter"
        v-model="text"
      >
        <template v-slot:prepend>
          <q-icon name="search" />
        </template>
      </q-input>
      <q-list separator padding>
        <q-item class="q-pa-md">
          <q-item-section>
            <q-item-label overline class="text=gray">Politics</q-item-label>
            <q-item-label class="text-weight-bold"
              >UK caught trying to steal French food</q-item-label
            >
            <q-item-label caption
              >The British people bored of their cuisine decided to cross the
              english tunnel and into france to try gourmet food but were caught
              in the act!</q-item-label
            >
          </q-item-section>

          <q-item-section side top>
            <q-item-label caption>5 min ago</q-item-label>
          </q-item-section>
        </q-item>
        <q-list bordered padding>
          <q-item class="q-pa-md">
            <q-item-section>
              <q-item-label overline class="text=gray">Politics</q-item-label>
              <q-item-label class="text-weight-bold"
                >UK caught trying to steal French food</q-item-label
              >
              <q-item-label caption
                >The British people bored of their cuisine decided to cross the
                english tunnel and into france to try gourmet food but were
                caught in the act!</q-item-label
              >
            </q-item-section>

            <q-item-section side top>
              <q-item-label caption>5 min ago</q-item-label>
            </q-item-section>
          </q-item>
        </q-list>
        <q-list bordered padding>
          <q-item class="q-pa-md">
            <q-item-section>
              <q-item-label overline class="text=gray">Politics</q-item-label>
              <q-item-label class="text-weight-bold"
                >UK caught trying to steal French food</q-item-label
              >
              <q-item-label caption
                >The British people bored of their cuisine decided to cross the
                english tunnel and into france to try gourmet food but were
                caught in the act!</q-item-label
              >
            </q-item-section>

            <q-item-section side top>
              <q-item-label caption>5 min ago</q-item-label>
            </q-item-section>
          </q-item>
        </q-list>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const leftDrawerOpen = ref(false);
    const rightDrawerOpen = ref(false);

    return {
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },

      rightDrawerOpen,
      toggleRightDrawer() {
        rightDrawerOpen.value = !rightDrawerOpen.value;
      },
    };
  },
};
</script>
