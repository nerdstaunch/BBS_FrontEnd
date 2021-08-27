<template>
  <v-card>
    <v-card-title>
      Create Board
    </v-card-title>

    <v-card-text>
      asdsa
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      id: 5,
      ip: null
    }
  },
  async mounted() {
      const ip = await this.$axios.$get('http://icanhazip.com')
      this.ip = ip
  }
}
</script>

<style>

</style>