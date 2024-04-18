<script>
import axios from 'axios';
import { api } from './store';

export default {
  data() {
    return {
      title: 'Vite Boolfolio',
      projects: [],
    }
  },

  created() {
    axios.get(store.api.baseUrl + 'project').then((response) => {
      this.projects = response.data.data;
    })
  }

  // components: {

  // }
}
</script>

<template>
  <div class="container">
    <h1>{{ title }}</h1>

    <div v-for="project in projects">
      <ul>
        <li><strong>ID: </strong> {{ project.id }}</li>
        <li><strong>Title: </strong> {{ project.title }}</li>
        <li><strong>Author: </strong> {{ project.author }}</li>
        <li><strong>Description: </strong> {{ project.description }}</li>
      </ul>

    </div>
  </div>
</template>

<style lang="scss">
@use '/src/scss/general.scss';
</style>