<template>
  <v-form>
    <v-container>
      <v-row>
        <!-- <v-col v-for="q in questions" v-bind:key="q.name" -->
        <v-col
          cols="12"
          md="4"
        >
          <v-text-field
            v-model="firstName"
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
          <v-radio-group v-model="moveOptions" row>
            <v-radio
              v-for="n in moveOptions"
              :key="n"
              :label="n"
              :value="n"
            ></v-radio>
          </v-radio-group>
      </v-row>
      <v-row>
      <v-col cols="12" md="12">
          <v-textarea
            outlined
            name="input-7-4"
            label="Brief description"
          ></v-textarea>
        </v-col>
      </v-row>
      <v-row>
        <v-text-field
            v-model="address"
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
            v-model="zipCOde"
            :counter="10"
            label="Zip Code"
            required
          ></v-text-field>
      </v-col>
      </v-row>
    </v-container>
  </v-form>
</template>

<script>
  export default {
    r: () => ({
      requiredRule: [
        v => !!v || 'Required',
      ]      
    }),
    data: () => ({
      // questions: [
      //   {name: "date", text: "When do you want to move?" },
      //   {name: "hours-estimated", text: "How many hours of help do you need?"},
      //   {name: "address", text: "Where can we meet you?"}
      // ],
      moveOptions: [
        "Load",
        "Unload",
        "Both",
        "Other"
      ],
      radioGroup: 1
    }),
  }
</script>