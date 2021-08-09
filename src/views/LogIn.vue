<template>
  <v-container class="fill-height" fluid>
    <v-row align="center" justify="center">
      <v-col cols="12" sm="8" md="5">
        <v-card class="elevation-12">
          <v-window v-model="step">
            <v-window-item :value="1">
              <v-row>
                <sign-in></sign-in>
                <v-col cols="12" md="4" class="teal accent-3">
                  <v-card-text class="white--text mt-12"
                    ><h1 class="text-center display-1">Sign Up</h1>
                    <h5 class="text-center mt-5">
                      Lorem ipsum dolor sit amet, consectetur adipiscing magna.
                      Sed nec suscipit purus, in facilisis augue.
                    </h5>
                  </v-card-text>
                  <div class="text-center mb-12">
                    <v-btn rounded outlined dark @click="step = 2">
                      Sign Up
                    </v-btn>
                  </div>
                </v-col>
              </v-row>
            </v-window-item>
            <v-window-item :value="2">
              <v-row class="fill-height">
                <v-col cols="12" md="4" class="teal accent-3">
                  <v-card-text class="white--text mt-12">
                    <h1 class="text-center display-1">Log In</h1>
                    <h5 class="text-center mt-5">
                      Lorem ipsum dolor sit amet, consectetur adipiscing magna.
                      Sed nec suscipit purus, in facilisis augue.
                    </h5>
                  </v-card-text>
                  <div class="text-center mt-12">
                    <v-btn rounded outlined dark @click="step = 1">
                      Log In
                    </v-btn>
                  </div>
                </v-col>
                <sign-up />
              </v-row>
            </v-window-item>
          </v-window>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import SignIn from "./SignIn.vue";
import SignUp from "./SignUp.vue";
export default {
  components: {
    SignIn,
    SignUp,
  },
  data: () => ({
    step: 1,
    showPassword: false,
  }),
  props: {
    source: String,
  },
};
</script>