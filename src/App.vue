<script>
import axios from 'axios';

export default {
  data() {
    return {
      title: 'Vite Boolfolio',
    }
  },

  created() {
    axios.get('').then((response) => { })
  }

  // components: {

  // }
}
</script>

<template>
  <h1>{{ title }}</h1>
</template>

<style lang="scss">
@use '/src/scss/general.scss';
</style>