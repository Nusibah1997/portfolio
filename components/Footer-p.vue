<template>
  <v-footer
    color="black lighten-1"
    padless
  >
    <v-row
      justify="center"
      no-gutters
    >
      <v-img src="/image/logo.png" max-width="300" max-height="80" contain />
      <v-btn
        v-for="link in links"
        :key="link"
        :to="link.to"
        color="white"
        text
        rounded
        class="my-2"
      >
        {{ link.title }}
      </v-btn>
      <v-col
        class="black lighten-2 py-4 text-center white--text"
        cols="12"
      >
        {{ new Date().getFullYear() }} — <strong>TECHNOREX</strong>
      </v-col>
    </v-row>
  </v-footer>
</template>

<script>
export default {
  name: 'FooterP',
  data: () => ({
    links: [
      { title: 'Home', to: '/' },
      { title: 'About Us', to: '/About-us' },
      { title: 'Services', to: '/Our-Services' },
      { title: 'Let`s Talk', to: '/connect-with-us' }
    ]
  })
}
</script>
