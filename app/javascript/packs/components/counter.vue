<template>
  <div id="app">
    <p>{{ message }}</p>
    Counter component 1 {{ count }}
    <button @click="increment"> +1 </button>
  </div>
</template>

<script>
  import {mapState, mapMutations} from 'vuex'
  
  export default {
    data: function () {
      return {
        message: "Hello Vue!"
      }
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
