<template>
  <v-app dark class="ma-0 pa-0">
    <div class="ma-auto text-center">
      <h1 v-if="error.statusCode === 404" class="grey--text">
        <v-img src="/image/bug.png" max-width="350" class="mb-3" />

        {{ pageNotFound }}
      </h1>
      <h1 v-else class="grey--text">
        <v-img src="/image/bug.png" max-width="350" class="mb-3" />
        {{ otherError }} {{ error.statusCode }}
      </h1>
      <v-btn
        nuxt
        to="/"
        rounded
        color="warning"
        large
        class="mt-4"
      >
        Home
      </v-btn>
    </div>
  </v-app>
</template>

<script>
export default {
  name: 'ErrorLayout',
  props: {
    error: {
      type: Object,
      default: null
    }
  },
  data () {
    return {
      pageNotFound: '404 Not Found',
      otherError: 'An error occurred'
    }
  },
  head () {
    const title =
      this.error.statusCode === 404 ? this.pageNotFound : this.otherError
    return {
      title
    }
  }
}
</script>

<style scoped>
h1 {
  font-size: 20px;
}
</style>
