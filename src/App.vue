<template>
  <div id="app">
    <script-example></script-example>
  </div>
</template>

<script>
import ScriptExample from "@/components/ScriptExample.vue";

export default {
  data() {
    return {
      tweets: [`tweet1`, `tweet2`, `tweet3`],
      num_friends: 42,
      logged_in: true,
    };
  },

  name: "App",
  components: {
    ScriptExample,
  },
};
</script>

<style>
</style>
