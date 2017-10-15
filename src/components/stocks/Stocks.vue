<template>
  <div>
    <app-stock v-for="stock in stocks" :stock="stock"></app-stock>
  </div>
</template>

<script>
  import Stock from './Stock.vue';
  import {
    mapActions,
    mapGetters,
    mapMutations,
    mapState
  } from 'vuex';

  export default {

    components: {
      appStock: Stock
    },
//
    computed: {
      ...mapGetters([
        //Getters from store
        'stocks'
      ]),
      ...mapState([
        //State from store
      ])
    },
    methods: {
      ...mapMutations([
        //Mutations from store
        'COUNT_PLUS',
        'COUNT_MINUS'
      ]),
      ...mapActions([
        //Actions from store
        'actionPlus',
        'actionMinus'
      ])
    }
  }

</script>