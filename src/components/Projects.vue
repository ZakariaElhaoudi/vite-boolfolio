<script>
import axios from 'axios';
import { onMounted } from 'vue';

export default {
  // name: 'Projects',
  data: function () {
    return {
      // projects: []
    }
  },

  mounted() {
    axios.get('http://localhost:8000/api/v1/project-index')
      .then(response => {
        console.log(response.data);
      })
      .catch(error => {
        console.log(error);
      });
  }
}





</script>

<template>
  ciao
</template>

<style scoped></style>
