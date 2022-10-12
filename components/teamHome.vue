<template>
  <div>
    <photo-p />
    <v-card-text>
      <p
        data-aos="zoom-in-down"
        class=" text-h2 text--primary font-weight-bold"
        align="center"
        justify="center"
      >
        Our Team
      </p>
    </v-card-text>
      <v-row dense>
        <v-col
          v-for="card in cards"
          :key="card.title"
          :cols="card.flex"
          md="4"
          class="scale"
          align="center"
          justify="center"
          data-aos="fade-down"
          data-aos-easing="linear"
          data-aos-duration="1500"
        >
          <v-img
            :src="card.src"
            max-width="400"
            max-height="300"
            class="rounded-circle align-center"
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
        </v-col>
      </v-row>
    <v-row
      class="my-4"
      align="center"
      justify="space-around"
    >
      <v-btn class="scale ma-2 py-12 font-weight-bold" text color="warning" nuxt :to="`/About-us`">
        SEE ALL OUR TEAM
      </v-btn>
    </v-row>
  </div>
</template>

<script>
import photoP from '~/components/photo-P'
export default {
  name: 'TeamHome',
  components: {
    photoP
  },
  data: () => ({
    cards: [
      { title: 'Ziad Omar', subtitle: 'Backend Developer', src: '/image/ziad.png', flex: 12 },
      { title: 'Jamil H', subtitle: 'Flutter Developer', src: '/image/jamil.png', flex: 12 },
      { title: 'Nusibah AL.Msallam', subtitle: 'Frontend Developer', src: '/image/nusibah.png', flex: 12 }
    ]
  })
}
</script>

<style scoped>
.scale:hover{
  transform: scale(1.3);
}
</style>
