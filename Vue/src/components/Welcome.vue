<template>
  <div class="greeting">
    <p v-if="showGreeting">{{greeting}}</p>
    <button v-on:click="toggleGreeting">Click me!</button>
  </div>
</template>

<script>
  export default {
    name: "welcome",
    data() {
      return {
        greeting: "Hello and Welcome!",
        showGreeting: false
      }
    },
    methods: {
      toggleGreeting() {
        this.showGreeting = !this.showGreeting
      }
    },

  }
</script>

<style scoped>
  .greeting {
    color: #00ffff;
  }
</style>
