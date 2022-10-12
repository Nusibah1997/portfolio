<template>
  <div>
    <div class="d-flex flex-no-wrap justify-center">
      <v-img
        src="/image/team.png"
        aspect-ratio="1.7"
        max-width="1000"
      />
    </div>
    <v-card
      class="mx-auto"
      justify="center"
    >
      <div class="d-flex flex-column justify-space-between align-center">
        <v-img
          data-aos="fade-up"
          data-aos-duration="3000"
          contain
          max-width="250"
          class=" justify-center "
          src="/image/logo.png"
        />
      </div>
      <v-card-text>
        <p
          data-aos="fade-right"
          data-aos-offset="300"
          data-aos-easing="ease-in-sine"
          class="text-h2 py-12 text--primary font-weight-bold"
          justify="center"
        >
          We focus on quality as a key point of differentiation
        </p>
      </v-card-text>
    </v-card>
    <v-card
      class="mx-auto"
    >
      <v-card-text>
        <p
          data-aos="fade-up"
          data-aos-duration="3000"
          class="text-h2 py-12 text--primary font-weight-bold"
          align="center"
          justify="center"
        >
          TEAM
        </p>
        <p
          data-aos="fade-up"
          data-aos-duration="3000"
          class="text-h4 align-center font-weight-bold"
          align="center"
          justify="center"
        >
          Meet our team members..
        </p>
      </v-card-text>
      <member-team />
    </v-card>
    <connect-with />
  </div>
</template>

<script>
import MemberTeam from '~/components/member-team'
import connectWith from '~/components/connect-with'
export default {
  name: 'IndexPage',
  components: {
    MemberTeam,
    connectWith
  }
}
</script>
