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
            :for="q.label"
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
      ],
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