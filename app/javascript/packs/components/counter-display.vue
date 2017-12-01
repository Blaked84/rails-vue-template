<template>
  <div id="counter-display">
    Counter component 2:
    {{ count }}
    and sqrt is: {{ sqrt }}
    <button @click="increment"> +1 </button>
    <button @click="incrementLater"> +1 later </button>
  </div>
</template>

<script>
  import {mapState, mapMutations, mapGetters, mapActions} from 'vuex'
  
  export default {
    computed: {
      ...mapState(['count']),
      ...mapGetters(['sqrt'])
    },
    methods: {
      ...mapMutations(['increment']),
      ...mapActions(['incrementLater'])
    }
  }
</script>
