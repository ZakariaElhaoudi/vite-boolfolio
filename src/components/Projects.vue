<script>
import axios from 'axios';
import { onMounted } from 'vue';

export default {
  // name: 'Projects',
  data: function () {
    return {
      projects: []
    }
  },

  mounted() {
    axios.get('http://localhost:8000/api/v1/project-index')
      .then(response => {
        this.projects = response.data.projects;
        console.log(response.data.projects);
        console.log(this.projects)
      })
      .catch(error => {
        console.log(error);
      });
  }
}





</script>

<template>
  <div class="container bg-dark">
    <div class="row">
      <div class="col-md-4 my-4" v-for="project in projects" :key="project.id">
        <div class="card">
          <div class="card-body">
            <h3 class="card-title">{{ project.name }}</h3>
            <h5 class="card-subtitle mb-2 text-muted">{{ project.author }}</h5>
            <p class="card-text">{{ project.description }}</p>
          </div>
        </div>
      </div>
    </div>

  </div>
</template>

<style scoped></style>
