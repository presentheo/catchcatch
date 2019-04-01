<template>
  <ul class="list-wrap">
    <li class="list">
      <div class="card" v-for="(fund, index) in funds" :key="index">
        <h1>{{fund.title}}</h1>
        <p>{{fund.desc}}</p>
      </div>
    </li>
  </ul>
</template>

<script lang="ts">
export default {
  name: 'Fund',
  data () {
    return {
      funds: [
        {
          title: 'Fund1',
          desc: String,
          startDate: Number,
          endDate: Number,
          fundGoal: Number
        },
        {
          title: 'fund2',
          desc: String,
          startDate: Number,
          endDate: Number,
          fundGoal: Number
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .list-wrap{
    display: flex;
  }
  .list{
    display: flex;
  }
  .card{
    border: 1px solid #ddd;
  }



</style>
