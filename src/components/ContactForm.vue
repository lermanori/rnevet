<template>
    <v-container>
        <v-layout justify-center>
            <v-flex xs7>
                <v-card>
                    <v-layout justify-center>
                        <v-card-title primary-title class="mx-auto">
                            <h3 class="headline mb-0 text-xs-center">Contact</h3>
                        </v-card-title>
                    </v-layout>
                    <v-form v-model="valid">
                        <v-container fluid>
                            <v-layout>
                                <v-flex xs12 md6>
                                    <v-text-field v-model="firstname" :rules="nameRules" :counter="10"
                                        label="First name" required></v-text-field>
                                </v-flex>

                                <v-flex xs12 md6>
                                    <v-text-field v-model="lastname" :rules="nameRules" :counter="10" label="Last name"
                                        required></v-text-field>
                                </v-flex>
                            </v-layout>
                            <v-layout>
                                <v-flex xs12 md12>
                                    <v-text-field v-model="email" :rules="emailRules" label="E-mail" required>
                                    </v-text-field>
                                </v-flex>
                            </v-layout>
                            <v-layout>
                                <v-flex xs12>
                                    <v-textarea outline name="input-7-1" label="Message" value=""
                                        hint="Enter Your Message"></v-textarea>
                                </v-flex>
                            </v-layout>
                            <v-layout justify-center>
                                    <v-btn :disabled="!valid" color="success" @click="validate">
                                        Validate
                                    </v-btn>

                                    <v-btn color="error" @click="reset">
                                        Reset Form
                                    </v-btn>

                                    <v-btn color="warning" @click="resetValidation">
                                        Reset Validation
                                    </v-btn>
                                </v-layout>
                        </v-container>
                    </v-form>
                </v-card>
            </v-flex>
        </v-layout>
    </v-container>
</template>

<script>
  export default {
    data: () => ({
      valid: true,
      firstname: '',
      lastname: '',
      nameRules: [
        v => !!v || 'Name is required',
        v => (v && v.length <= 10) || 'Name must be less than 10 characters'
      ],
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+/.test(v) || 'E-mail must be valid'
      ],

    }),

    methods: {
      validate () {
        if (this.$refs.form.validate()) {
          this.snackbar = true
        }
      },
      reset () {
        this.$refs.form.reset()
      },
      resetValidation () {
        this.$refs.form.resetValidation()
      }
    }
  }
</script>

<style>

</style>