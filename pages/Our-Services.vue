<template>
  <div>
    <div class="d-flex flex-no-wrap justify-space-between">
      <v-row>
        <v-col
          cols="12"
          md="6"
        >
          <div>
            <v-card-title
              data-aos="fade-right"
              data-aos-offset="300"
              data-aos-easing="ease-in-sine"
              class="text-h1 font-weight-bold pt-10"
            >
              Products
            </v-card-title>
          </div>
        </v-col>
        <v-col
          cols="12"
          md="6"
        >
          <v-img
            data-aos="fade-down"
            data-aos-easing="linear"
            data-aos-duration="1500"
            src="/image/products.png"
            aspect-ratio="1.7"
            max-width="800"
          />
        </v-col>
      </v-row>
    </div>
    <v-card-title>
      <v-card-text>
        <p
          data-aos="fade-up"
          data-aos-duration="3000"
          class="px-16 text-h4 py-12 text--primary font-weight-bold"
          align="center"
          justify="center"
        >
          Whether you’ve already identified a transformation roadmap and need help to rapidly execute, or, you’re ready to start looking at what opportunities are out there, we offer a full service approach to building your next digital venture.
        </p>
      </v-card-text>
    </v-card-title>
    <our-products />
    <connect-with />
  </div>
</template>

<script>
import ourProducts from '~/components/our-products'
import connectWith from '~/components/connect-with'
export default {
  name: 'IndexPage',
  components: {
    ourProducts,
    connectWith
  }
}
</script>

<style>

</style>
