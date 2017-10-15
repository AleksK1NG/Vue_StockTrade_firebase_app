<template>
  <div>
    <h1>Trade or view your portfolio</h1>
    <h5>You can Save & Load your Data</h5>
    <h5>You can click on 'End Day' to begin a New Day !</h5>
    <hr>
    <p>Your money: {{ funds | currency }} </p>
  </div>

</template>

<script>

  export default {
    computed: {
      funds() {
        return this.$store.getters.funds;
      }
    }
  }

</script>