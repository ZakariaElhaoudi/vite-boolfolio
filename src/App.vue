<script>
import axios from 'axios';
import Projects from './components/Projects.vue'

export default {
  components: {
    Projects
  },
  data: function () {
    return {
    }
  },
}
</script>

<template>
  <div class="container-fluid text-center">
    <h1>Projects</h1>
  </div>
  <Projects />
</template>

<style scoped></style>
