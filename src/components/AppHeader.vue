<script>
import axios from 'axios';

export default {
  data: function () {
    return {
    }
  },
}
</script>

<template>
  <div class="container-fluid text-center bg-dark text-white py-3 justify-content-between">
    <h1>HEADER</h1>
    <h2>
      <router-link :to="{ name: 'home' }">HOME</router-link>
    </h2>
  </div>
</template>

<style scoped></style>
