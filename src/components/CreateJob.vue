<template>
  <v-form>
    <v-container>
      <v-row>
        <v-col v-for="q in questions" v-bind:key="q.name"
          cols="12"
          md="4"
        >
          <v-text-field
            v-model="q.text"
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
            v-model="lastname"
            :rules="nameRules"
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
            :rules="phoneRules"
            label="Phone"
            required
          ></v-text-field>
        </v-col>
      </v-row>
      <v-row>
          <v-radio-group v-model="moveOptions">
        <v-col>
            <v-radio
              v-for="n in moveOptions"
              :key="n"
              :label="n"
              :value="n"
            ></v-radio>
        </v-col>
          </v-radio-group>
      </v-row>
    </v-container>
  </v-form>
</template>

<script>
  export default {
    r: () => ({
      requiredRule: [
        v => !!v || 'Required',
      ],
      radioGroup: 1,
      moveOptions: [
        "Load",
        "Unload",
        "Both",
        "Other"
      ]
    }),
    data: () => ({
      questions: [
        {name: "date", text: "When do you want to move?" },
        {name: "hours-estimated", text: "How many hours of help do you need?"},
        {name: "address", text: "Where can we meet you?"}
      ]
    }),
  }
</script>