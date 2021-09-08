<template>
  <div>
  <p>You have watched to episode: {{ init_cnt }}. You should watch another episode today.</p>
    <button v-on:click="init_cnt -= 1">decrements</button>
    <button v-on:click="init_cnt += 1">increments</button>
    </div>
</template>

<script>
export default {
  props:['init_cnt'],
  data() {
    return {
      init_cnt
    };
  }
};
</script>

<style>
</style>

