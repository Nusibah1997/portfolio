<template>
  <v-container fluid>
    <v-col
      v-for="card in cards"
      :key="card.title"
      :cols="card.flex"
    >
      <v-card
        class="mx-auto"
        height=""
      >
        <div class="d-flex flex-no-wrap justify-space-between">
          <v-row>
            <v-col
              cols="12"
              md="6"
            >
              <div>
                <v-card-subtitle
                  data-aos="fade-right"
                  data-aos-offset="300"
                  data-aos-easing="ease-in-sine"
                  class="text-h5"
                  v-text="card.artist"
                />
                <v-card-title
                  data-aos="fade-right"
                  data-aos-offset="300"
                  data-aos-easing="ease-in-sine"
                  class="text-h3"
                  v-text="card.title"
                />
                <v-card-subtitle
                  data-aos="fade-right"
                  data-aos-offset="300"
                  data-aos-easing="ease-in-sine"
                  class="text-h7"
                  v-text="card.summary"
                />
                <v-card-actions>
                  <v-btn
                    :key="card.to"
                    data-aos="fade-right"
                    data-aos-offset="300"
                    data-aos-easing="ease-in-sine"
                    class="ma-2 py-12"
                    text
                    color="warning"
                    nuxt
                    :to="card.to"
                  >
                    <v-icon color="blue-grey" large>
                      mdi-web
                    </v-icon>
                    LinkedIn Profile
                  </v-btn>
                </v-card-actions>
              </div>
            </v-col>
            <v-col
              cols="12"
              md="6"
            >
              <v-avatar
                data-aos="fade-down"
                data-aos-easing="linear"
                data-aos-duration="1500"
                class="ma-3"
                size="400"
                tile
              >
                <v-img
                  class="white--text align-end"
                  height="400px"
                  :src="card.src"
                />
              </v-avatar>
            </v-col>
          </v-row>
        </div>
      </v-card>
    </v-col>
  </v-container>
</template>

<script>
export default {
  name: 'MemberTeam',
  data: () => ({
    cards: [
      {
        title: 'PROJECT1',
        artist: 'Backend Developer',
        src: '/image/ziad.png',
        summary: 'Involvement: Technical Leader, Digital Transformation, Systems Design interests: Coaching, New Technologies and Product Management.Saed is a seasoned product manager and oversees delivery of bespoke applications for large public and private clients.',
        flex: 12
      },
      {
        title: 'PROJECT2',
        artist: 'Flutter Developer',
        src: '/image/jamil.png',
        summary: 'Involvement: Technical Leader, Digital Transformation, Systems Design interests: Coaching, New Technologies and Product Management.Saed is a seasoned product manager and oversees delivery of bespoke applications for large public and private clients.',
        flex: 12
      },
      {
        title: 'PROJECT3',
        artist: 'Frontend Developer',
        src: '/image/nusibah.png',
        summary: 'Involvement: Technical Leader, Digital Transformation, Systems Design interests: Coaching, New Technologies and Product Management.Saed is a seasoned product manager and oversees delivery of bespoke applications for large public and private clients.',
        flex: 12
      }
    ]
  })
}
</script>
