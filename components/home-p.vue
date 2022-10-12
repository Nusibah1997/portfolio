<template>
  <div class="d-flex flex-no-wrap justify-space-between pt-10">
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
            class="justify-center text-h1 font-weight-bold pt-10"
          >
            We buid
          </v-card-title>
          <div class="px-16 flex-no-wrap justify-center">
            <p
              class="px-16 warning text-h2 font-weight-bold secondary--text d-flex flex-nowrap"
              data-aos="zoom-in-right"
            >
              Digital businesses
            </p>
            <p
              class="px-16 text-h2 font-weight-bold flex-wrap"
              data-aos="fade-up"
              data-aos-duration="3000"
            >
              for industry leaders
            </p>
          </div>
        </div>
        <photo-p />
      </v-col>
      <v-col
        cols="12"
        md="6"
      >
        <div class="ma-16">
          <point-p />
          <v-img
            data-aos="fade-down"
            data-aos-easing="linear"
            data-aos-duration="1500"
            src="/image/home.svg"
            aspect-ratio="1"
            max-width="700"
          />
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import pointP from '~/components/Point-p'
export default {
  name: 'HomeP',
  components: {
    pointP
  }
}
</script>
