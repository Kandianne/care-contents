<template >
  <v-form id="new-job" @submit.prevent="submitForm">
    <v-container>
      <v-row>
        <v-col
          cols="12"
          md="4"
        >
          <v-text-field
            v-model="firstName"
            name="firstName"
            :counter="10"
            label="First name"
            required
          ></v-text-field>
        </v-col>
        <v-col
          cols="12"
          md="4"
        >
          <v-text-field
            v-model="lastName"
            :counter="10"
            label="Last name"
            required
          ></v-text-field>
        </v-col>

        <v-col
          cols="12"
          md="4"
        >
          <v-text-field
            v-model="phone"
            label="Phone"
            required
          ></v-text-field>
        </v-col>
      </v-row>
      <v-row>
          <v-radio-group v-model="active" row>
            <v-radio v-for="n in moveOptions" :key="n"
              :label="n"
              :value="n" type="radio" v-model="moveOptionSelected"></v-radio>
          </v-radio-group>
      </v-row>
      <v-row>
      <v-col cols="12" md="12">
          <v-textarea
            outlined
            v-model="briefDescription"
            name="input-7-4"
            label="Brief description"
          ></v-textarea>
        </v-col>
      </v-row>
      <v-row>
        <v-text-field
            v-model="address1"
            :counter="10"
            label="Street address"
            required
          ></v-text-field>
      </v-row>
      <v-row>
        <v-text-field
            v-model="address2"
            :counter="10"
            label="Street address 2"
            required
          ></v-text-field>
      </v-row>
      <v-row>
      <v-col cols="12" md="4">
        <v-text-field
            v-model="city"
            :counter="10"
            label="City"
            required
          ></v-text-field>
      </v-col>
      <v-col cols="12" md="4">
          <v-text-field
            v-model="state"
            :counter="10"
            label="State"
            required
          ></v-text-field>
      </v-col>
      <v-col cols="12" md="4">
           <v-text-field
            v-model="zipCode"
            :counter="10"
            label="Zip Code"
            required
          ></v-text-field>
      </v-col>
      </v-row>
      <v-row>
        <button type="submit">Send Info</button>
      </v-row>
    </v-container>
    {{ $data }}
  </v-form>
</template>

<script>
import emailjs from 'emailjs-com';

  export default {
    r: () => ({
      requiredRule: [
        v => !!v || 'Required',
      ]      
    }),
    data: () => ({
      moveOptions: [
        "Load",
        "Unload",
        "Both",
        "Other"
      ],
      radioGroup: 1,
      firstName: "",
      lastName: "",
      phone: 0,
      briefDescription: "",
      address1: "",
      address2: "",
      city: "",
      state: "",
      zipCode: "",
      moveOptionSelected: ""
    }),
    methods: {
      submitForm (e) {
            console.log(this)
        //  emailjs.sendForm('carefulcontentsmovers', 'template_9hxRp4gy', this.firstName, 'user_y0vRaKJBiVvgsBXJpxxN0')
        // .then((result) => {
        //     alert('SUCCESS!', result);
        // }, (error) => {
        //     alert(error)
        // });
        // alert(this.moveOptionSelected)
      }
    }

  }
</script>