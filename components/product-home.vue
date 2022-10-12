<template>
  <div>
    <v-card-text>
      <p
        data-aos="zoom-in-down"
        class=" text-h2 text--primary font-weight-bold"
        align="center"
        justify="center"
      >
        Products
      </p>
      <p
        class=" text-h4  warning--text "
        align="center"
        justify="center"
        data-aos="fade-up"
        data-aos-anchor-placement="top-bottom"
      >
        What our team offer
      </p>
    </v-card-text>
      <v-row jsutif="center">
        <v-col
          v-for="card in cards"
          :key="card.title"
          :cols="card.flex"
          md="4"
          data-aos="fade-down"
          data-aos-easing="linear"
          data-aos-duration="1500"
        >
          <v-card
            class="scale mx-7"
            shaped
          >
            <v-img
              :src="card.src"
              max-width="200"
              class="d-block"
              contain
              aspect-ratio="1.5"
            />
            <v-card-title
              class="d-block accent--text font-weight-bold"
              align="center"
              justify="center"
              v-text="card.title"
            />
            <v-card-subtitle
              class="accent--text font-weight-bold"
              align="center"
              justify="center"
              v-text="card.subtitle"
            />
          </v-card>
        </v-col>
      </v-row>
    <v-spacer />
    <v-row
      class="my-4"
      align="center"
      justify="space-around"
    >
      <v-btn class="scale font-weight-bold ma-2 py-12" text color="warning" nuxt :to="`/Our-Services`">
        SEE ALL PRODUCTS
      </v-btn>
    </v-row>
  </div>
</template>

<script>
export default {
  data: () => ({
    cards: [
      { title: 'DISCOVER', subtitle: 'Data-led Roadmapping', src: '/image/descover.png', flex: 12 },
      { title: 'DEFINE', subtitle: 'From Strategy to Product', src: '/image/defind.png', flex: 12 },
      { title: 'DESIGN', subtitle: 'Experience > Interface', src: '/image/design.png', flex: 12 }
    ]
  })
}
</script>

<style scoped>
.scale:hover{
     transform: scale(1.1)
}
</style>
