<template>
  <div class="field">
    <Note v-for="n in 5" :key="n"></Note>
  </div>
</template>

<script lang="ts">
import Note from './Note.vue';

export default {
  name: 'Field',
  components: {
    Note
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>

.field{
  width: 500px;
  height: 500px;
  margin: auto;
  border: 2px solid #ddd;
  position: relative;
}

</style>
