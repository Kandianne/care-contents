<template>
<main>
  <Home />
  <CreateJob />
</main>
</template>

<script>
import Home from './components/Home';
import CreateJob from './components/CreateJob';

export default {
  name: 'App',

  components: {
    Home,
    CreateJob
  },

  data: () => ({
    //
  }),
};
</script>

<style scoped>
</style>
