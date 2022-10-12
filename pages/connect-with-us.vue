<template>
  <div>
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
              class="justify-center text-h2 font-weight-bold pt-10"
            >
              Let’s Talk
            </v-card-title>
            <div class="px-16 flex-no-wrap justify-center">
              <p
                class="px-16 text-h5 d-flex flex-wrap"
                data-aos="fade-right"
                data-aos-offset="300"
                data-aos-easing="ease-in-sine"
              >
                Have a project you want to discuss?
              </p>
              <p
                class="px-16 flex-wrap"
                data-aos="fade-up"
                data-aos-duration="3000"
              >
                Send us a Request for Information
              </p>
            </div>
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
            src="/image/SentMessage.png"
            aspect-ratio="1"
            max-width="700"
          />
        </v-col>
      </v-row>
    </div>
    <sent-email />
  </div>
</template>

<script>
import sentEmail from '~/components/sent-email'
export default {
  name: 'IndexPage',
  components: {
    sentEmail
  }
}
</script>

<style scoped >
.p{
  color: #FFE082;
}
</style>
