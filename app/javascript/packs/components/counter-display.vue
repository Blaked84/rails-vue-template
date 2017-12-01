<template>
  <div id="counter-display">
    Counter component 2:
    {{ count }}
    and sqrt is: {{ sqrt }}
    <button @click="increment"> +1 </button>
  </div>
</template>

<script>
  import {mapState, mapMutations, mapGetters} from 'vuex'
  
  export default {
    computed: {
        ...mapState(['count']),
        ...mapGetters(['sqrt'])
    },
    methods: {
      ...mapMutations(['increment'])
    }
  }
</script>
