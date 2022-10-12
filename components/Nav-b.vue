<template>
  <v-card class="overflow-hidden">
    <v-app-bar
      class="app-bar v-app-bar--fixed"
      color="#fff"
      shrink-on-scroll
      scroll-target="#scrolling-techniques-2"
      lights-out
      dense
    >
      <v-img
        src="/image/logo.png"
        px-0
        py-10
        max-width="100"
        contain
      />
      <v-app-bar-title class="font-weight-bold py-6">
        TECHNOREX
      </v-app-bar-title>
      <v-tabs align-with-title class="hidden-xs-only mx-12" text color="accent">
        <v-spacer />
        <v-tab><a class="font-weight-bold black--text" href="/">Home</a></v-tab>
        <v-tab>
          <nuxt-link class="font-weight-bold black--text" to="/About-us">
            About Us
          </nuxt-link>
        </v-tab>
        <v-tab>
          <nuxt-link class="font-weight-bold black--text" to="/Our-Services">
            Services
          </nuxt-link>
        </v-tab>
        <v-tab>
          <nuxt-link class="font-weight-bold black--text" to="/connect-with-us">
            Let's Talk
          </nuxt-link>
        </v-tab>
      </v-tabs>
      <v-spacer />
      <div class="hidden-sm-and-up">
        <template>
          <v-app-bar-nav-icon @click="drawer = true" />

          <v-navigation-drawer
            v-model="drawer"
            absolute
            temporary
            height="100%"
            width="100%"
          >
            <v-list
              rounded
              class="mt-8 mb-8"
              nav
              dense
            >
              <template v-for="(item) in items">
                <v-list-item
                  :key="item.to"
                  exact-path
                  :to="item.to"
                  dense
                >
                  <v-list-item-avatar height="30px">
                    <v-icon>{{ item.icon }}</v-icon>
                  </v-list-item-avatar>
                  <v-list-item-content class="my-0 py-0">
                    <v-list-item-title>
                      {{ item.title }}
                    </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </template>
            </v-list>
          </v-navigation-drawer>
        </template>
      </div>
    </v-app-bar>
    <v-sheet
      id="scrolling-techniques-2"
      class="overflow-y-auto"
      max-height="600"
    >
      <v-container style="height: 90px;" />
    </v-sheet>
  </v-card>
</template>

<script>
import { mdiHome, mdiAccountGroup, mdiPhone, mdiShopping } from '@mdi/js'
export default {
  name: 'NavB',
  data: () => ({
    drawer: false,
    group: null,
    items: [
      { title: 'Home', icon: mdiHome, to: '/' },
      { title: 'About Us', icon: mdiAccountGroup, to: '/About-us' },
      { title: 'Services', icon: mdiShopping, to: '/Our-Services' },
      { title: 'Let\'s Talk', icon: mdiPhone, to: '/connect-with-us' }
    ]
  })
}
</script>

<style scoped>
.v-app-bar-title__content{
  width: 130px;
}
</style>
