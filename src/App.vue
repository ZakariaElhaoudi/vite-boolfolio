<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue'
export default {
  components: {
    AppHeader
  },
  data: function () {
    return {
    }
  },
}
</script>

<template>
  <AppHeader />
  <router-view></router-view>
</template>

<style scoped></style>
