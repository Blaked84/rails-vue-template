<template>
  <div id="app">
    <counter></counter>
    <counter-display></counter-display>
  </div>
</template>

<script>
  import {mapState, mapMutations} from 'vuex'
  import Counter from './counter'
  import CounterDisplay from './counter-display'
  
  export default {
    data: function () {
      return {
        message: "Hello Vue!"
      }
    },
    components: {
      'counter': Counter,
      'counter-display': CounterDisplay
    },
    computed: mapState(['count']),
    methods: {
      ...mapMutations(['increment'])
    }
  }
</script>

<style scoped>
p {
  font-size: 2em;
  text-align: center;
}
</style>
