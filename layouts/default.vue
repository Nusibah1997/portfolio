<template>
  <v-app>
    <nav-b />
    <v-main>
      <Nuxt />
    </v-main>
    <Footer-p />
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
    }
  }
}
</script>

<style>
* {
  font-family: 'Bad Script', 'cursive' !important;
}
</style>
