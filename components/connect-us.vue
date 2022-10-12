<template>
  <div
    class="mx-auto"
  >
    <v-card-text>
      <p
        data-aos="zoom-in-down"
        class="text-h2 py-12 text--primary font-weight-bold"
        align="center"
        justify="center"
      >
        Let's Connect!
      </p>
    </v-card-text>
    <v-container>
      <v-row dense>
        <v-col
          v-for="(item, i) in items"
          :key="i"
          cols="12"
        >
          <div class="d-flex flex-no-wrap justify-space-between">
            <v-row>
              <v-col
                cols="12"
                md="7"
              >
                <div>
                  <v-card-title
                    data-aos="fade-right"
                    transition="fab-transition"
                    class="text-h4 font-weight-bold mt-0"
                  >
                    SEE WHAT WE CAN BUILD FOR YOU
                  </v-card-title>
                  <v-card-actions>
                    <div data-aos="fade-right">
                      <v-icon color="warning">
                        mdi-arrow-right-thick
                      </v-icon>
                      <v-btn
                        class="scale font-weight-bold ml-2 mt-0"
                        text
                        color="warning"
                        :to="`/connect-with-us`"
                      >
                        Go ahead give us your wishlist
                      </v-btn>
                    </div>
                    <point-p />
                  </v-card-actions>
                </div>
              </v-col>
              <v-col
                cols="12"
                md="5"
              >
                <v-avatar
                  class="ma-3"
                  size="300"
                  tile
                >
                  <v-img
                    data-aos="fade-down"
                    data-aos-easing="linear"
                    data-aos-duration="1500"
                    :src="item.src"
                    max-width="600"
                  />
                </v-avatar>
              </v-col>
            </v-row>
          </div>
        </v-col>
      </v-row>
    </v-container>
    <connect-with />
  </div>
</template>

<script>
import connectWith from '~/components/connect-with'
import pointP from '~/components/Point-p'
export default {
  name: 'ConnectUs',
  components: {
    connectWith,
    pointP
  },
  data: () => ({
    items: [
      {
        color: '#1F7087',
        src: '/image/connect.png'
      }
    ],
    color: '#FFC107'
  })
}
</script>
<style scoped>
.ma-2{
  background-color: white;
}
.scale:hover{
  transform: scale(1.3);
}
</style>
