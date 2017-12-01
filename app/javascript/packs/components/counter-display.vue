<template>
  <div id="counter-display">
    Counter component 2:
    {{ count }}
    <button @click="increment"> +1 </button>
  </div>
</template>

<script>
  import {mapState, mapMutations} from 'vuex'
  
  export default {
    computed: mapState(['count']),
    methods: {
      ...mapMutations(['increment'])
    }
  }
</script>
