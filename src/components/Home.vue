<template>
  <div class="home">
    <div v-for="ride in api" class="ride">
      {{ride.line.name}}
      {{ride.direction}}
      {{ride.when}}
    </div>
    {{api}} 
  </div>
</template>

<script>

import json from './../data/data.json'
export default {
  name: 'Home',
  data () {
    return {
      api: json
    }
  }
}
</script>

<style scoped lang="sass">
.home
  .ride
    margin: 1em
</style>
