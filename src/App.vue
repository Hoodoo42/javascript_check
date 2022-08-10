<template>
  <div id="app">
    <h3>Numer of friends:{{ num_friends }}</h3>

    <script-example></script-example>
  </div>
</template>

<script>
import ScriptExample from "@/components/ScriptExample.vue";

export default {
  methods: {
    show_info() {
      if (this.logged_in) {
        document.body.insertAdjacentHTML(
          `afterbegin`,
          `
    <h4>You are logged in</h4>
    `
        );
      } else {
        document.body.insertAdjacentHTML(
          `afterbegin`,
          `
    <h4>You are not logged in</h4>`
        );
      }

      for (let i = 0; i < this.tweets.length; i++) {
        document.body.insertAdjacentHTML(
          `beforeend`,
          `
      <h4>${this.tweets[i]}</h4>`
        );
      }
    },
  },

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

  mounted: function () {
    this.show_info();
  },
};
</script>

<style>
</style>
