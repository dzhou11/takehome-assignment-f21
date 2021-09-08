<template>
  <!-- PART 4: Add your code here -->
  <div>
    <hr>
    <p>Show name: {{name}}
    </p>
    <Counter init_cnt=1 />
  </div>
</template>

<script>
// PART 4: Add your code here
import Counter from "./Counter.vue"

export default {
    components:{
        Counter
        },

    props:['id','name','episode_seen']

    };
</script>

<style>
</style>
