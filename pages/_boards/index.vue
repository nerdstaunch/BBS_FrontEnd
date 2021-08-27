<template>
  <div>
    BOARD
    
    <div v-for="(tutorial, index) of tutorials" :key="index">
      {{tutorial}}
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      test: 'ad',
      route: this.$route,
      tutorials: null
    }
  },
  async mounted() {
    const ip = await this.$axios.$get('http://localhost:8080/api/tutorials')
    this.tutorials = ip;

  }
}
</script>

<style>

</style>