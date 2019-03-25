<template>
  <transition appear @appear="setInitialStyle" @after-appear="this.fadeIn">
    <div class="note" @click="this.catch" ></div>
  </transition>
</template>

<script lang="ts">
export default {
  data () {
    return {
      caught: false
    }
  },
  methods: {
    catch() {
      this.caught = true;
      this.$el.style.backgroundColor = 'white'
    },
    setInitialStyle() {
      this.$el.style.opacity = 0;
    },
    fadeIn() {
      setTimeout(() => {
        this.$el.style.opacity = 1;
        this.$el.style.left = Math.floor(Math.random()*400) + 'px';
        this.$el.style.top = Math.floor(Math.random()*400) + 'px';
        this.$el.style.transition = 'opacity 1s ease';
      }, Math.floor(Math.random()*3000))
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>

.note{
  width: 100px;
  height: 100px;
  margin: 4px;
  background-color: black;
  border-radius: 10%;
  border: 1px white solid;
  position: absolute;
}

</style>
