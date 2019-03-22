<template>
  <div class="ball" @click="this.catch">
  </div>
</template>

<script lang="ts">
export default {
  name: 'Ball',
  data () {
    return {
      caught: false
    }
  },
  methods: {
    catch() {
      this.caught = !this.caught
      alert(this.caught);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.ball{
  width: 100px;
  height: 100px;
  border-radius: 50%;
  background-color: black;
}

</style>
