<template>
  <v-col cols="12" md="8">
    <v-card-text class="mt-12"
      ><h1 class="text-center display-2 teal--text text-accent-3 mb-10">
        Log In
      </h1>
      <v-form>
        <v-text-field
          prepend-icon="mdi-email"
          class="mx-5"
          outlined
          label="Email"
          name="Email"
          type="email"
          color="teal accent-3"
        />
        <v-text-field
          prepend-icon="mdi-lock"
          class="mx-5"
          color="teal accent-3"
          outlined
          :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
          :type="showPassword ? 'text' : 'password'"
          name="input-10-1"
          label="Password"
          @click:append="showPassword = !showPassword"
        ></v-text-field>
      </v-form>
    </v-card-text>
    <div class="text-center mb-10">
      <v-btn rounded color="teal accent-3" dark>Log In</v-btn>
    </div>
  </v-col>
</template>

<script>
export default {
  data: () => ({
    showPassword: false,
  }),
};
</script>
