<template>
  <v-form
    ref="form"
    v-model="valid"
  >
    <v-container>
      <v-row>
        <v-col
          data-aos="fade-up"
          data-aos-anchor-placement="top-bottom"
          cols="12"
          sm="6"
        >
          <v-text-field
            v-model="first"
            data-aos="fade-up"
            data-aos-anchor-placement="top-bottom"
            label="First Name"
            outlined
            shaped
          />
        </v-col>

        <v-col
          data-aos="fade-up"
          data-aos-anchor-placement="top-bottom"
          cols="12"
          sm="6"
        >
          <v-text-field
            v-model="last"
            label="Last Name"
            outlined
            shaped
          />
        </v-col>
        <v-col
          cols="12"
          sm="6"
          data-aos="fade-up"
          data-aos-anchor-placement="top-bottom"
        >
          <v-text-field
            v-model="email"
            :rules="[rules.email]"
            color="deep-purple"
            label="Email address"
            type="email"
            outlined
            shaped
            @input="$v.email.$touch()"
            @blur="$v.email.$touch()"
          />
        </v-col>

        <v-col
          cols="12"
          sm="6"
          data-aos="fade-up"
          data-aos-anchor-placement="top-bottom"
        >
          <v-text-field
            v-model="phone"
            color="deep-purple"
            label="Phone number"
            outlined
            shaped
          />
        </v-col>
        <v-col
          cols="12"
          data-aos="fade-up"
          data-aos-anchor-placement="top-bottom"
        >
          <v-textarea
            v-model="Message"
            auto-grow
            outlined
            color="deep-purple"
            label="Message"
            rows="5"
            shaped
          />
        </v-col>
        <v-card-actions>
          <v-btn
            text
            @click="reset"
          >
            Clear
          </v-btn>
          <v-spacer />
          <v-btn
            class="white--text"
            color="amber darken-2"
            depressed
            @click="submit"
          >
            Send
          </v-btn>
        </v-card-actions>
      </v-row>
    </v-container>
  </v-form>
</template>

<script>
export default {
  data: () => ({
    valid: true,
    first: 'John',
    last: 'Doe',
    Message: '',
    phone: undefined,
    email: undefined,
    form: false,
    rules: {
      email: v => !!(v || '').match(/@/) || 'Please enter a valid email'
    }
  }),
  methods: {
    submit () {
      this.$refs.form.submit()
    },
    reset () {
      this.$refs.form.reset()
    }
  }
}
</script>
