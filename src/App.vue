<script>
import axios from 'axios';
import { api, store } from './store';
import ProjectCard from "./components/ProjectCard";

export default {
  data() {
    return {
      title: 'Vite Boolfolio',
      store,
    };
  },

  components: { ProjectCard },

  created() {
    axios.get(store.api.baseUrl + 'project').then((response) => {
      store.projects = response.data.data;
    });
  },
};
</script>

<template>
  <div class="container">
    <h1>{{ title }}</h1>

    <!-- <div v-for="project in store.projects">
      <ul>
        <li><strong>ID: </strong> {{ project.id }}</li>
        <li><strong>Title: </strong> {{ project.title }}</li>
        <li><strong>Author: </strong> {{ project.author }}</li>
        <li><strong>Description: </strong> {{ project.description }}</li>
      </ul>

    </div> -->
  </div>
</template>

<style lang="scss">
@use '/src/scss/general.scss';
</style>