<template>
  <div id="app">
    <p>{{ message }}</p>
    {{ count }}
    <button @click="increment"> +1 </button>
  </div>
</template>

<script>
  import {mapState} from 'vuex'
  
  export default {
    data: function () {
      return {
        message: "Hello Vue!"
      }
    },
    computed: mapState(['count']),
    methods: {
      increment() {
        this.$store.commit('increment')
      }
    }
  }
</script>

<style scoped>
p {
  font-size: 2em;
  text-align: center;
}
</style>
