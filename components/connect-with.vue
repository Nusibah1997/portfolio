<template>
  <div>
    <v-sheet
      color="warning"
      height="500"
      tile
    >
      <div
        data-aos="fade-up"
        data-aos-duration="3000"
        class="fill-height py-12"
        align="center"
        justify="center"
      >
        <div class="text-h2  py-12 align-content-center fab-transition"
             data-aos="fade-up"
             data-aos-duration="3000"
        >
          Say Hi and let's create something
        </div>
        <div class="text-h3 align-center font-weight-bold"
             data-aos="fade-up"
             data-aos-duration="3000"
        >
          great together
        </div>
        <v-row
          class="my-4 py-12"
          align="center"
          justify="space-around"
        >
          <v-hover
            v-slot="{ hover }"
            open-delay="200"
          >
            <v-btn
              class="ma-2 px-10"
              :elevation="hover ? 16 : 2"
              :class="{ 'on-hover': hover }"
              text
              outlined
              rounded
              nuxt
              color="warning"
              x-large
              :to="`/connect-with-us`"
            >
              Let's talk
            </v-btn>
          </v-hover>
        </v-row>
      </div>
    </v-sheet>
  </div>
</template>

<script>
export default {
  name: 'ConnectWith'
}
</script>

<style scoped>
.ma-2{
  background-color: white;
}
</style>
