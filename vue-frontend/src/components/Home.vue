<template>
  <div>
    <!-- PART 1: Pass in a "complete" prop here -->
    <Instructions
    complete="hi"/>
    <!-- PART 4: Modify the Show component to accept all of these props -->
    <form action="/shows">
        <label for="name">New show name(not working):</label>
        <input type="text" id="name" name="name">
        <input type="submit" href="/shows">
    </form>

    <Show
      v-for="show in shows"
      :key="show.id"
      :id="show.id"
      :name="show.name"
      :episodes_seen="show.episodes_seen"
    />
  </div>
</template>

<script>
import Instructions from "./Instructions.vue";
import Show from "./Show.vue";
 

export default {
  components: {
    Instructions,
    Show
  },
  data() {
    return {
      shows: [
        { id: 1, name: "Game of Thrones", episodes_seen: 0 },
        { id: 2, name: "Naruto", episodes_seen: 220 },
        { id: 3, name: "Black Mirror", episodes_seen: 3 }
      ]
    };
  }
};
</script>

<style>
</style>


