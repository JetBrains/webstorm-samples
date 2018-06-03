<template>
  <div>
    <Logo/>
    <div class="greeting">
      <p v-if="showGreeting">{{greeting}}</p>
      <button v-on:click="toggleGreeting">Click me!</button>
    </div>
  </div>
</template>

<script>
  import Logo from "@/components/Logo";

  export default {
    name: 'HelloWorld',
    components: {Logo},
    data() {
      return {
        msg: 'Welcome to Your Vue.js App',
        greeting: "Hello and Welcome!",
        showGreeting: false
      }
    },
    methods: {
      toggleGreeting() {
        this.showGreeting = !this.showGreeting;
      }
    }
  }
</script>

<style scoped>
  h1, h2 {
    font-weight: normal;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }
</style>
