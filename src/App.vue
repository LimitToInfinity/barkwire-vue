<template>
  <div id="app">
    <Incrementer 
      :count="count"
      @increment="increment"
      @decrement="decrement"
    />
  </div>
</template>

<script>
  import Incrementer from "@/components/Incrementer"

  export default {
    components: {
      Incrementer,
    },
    data() {
      return {
        count: 1
      }
    },
    methods: {
      increment(amount) {
        this.count = this.count + amount
      },
      decrement(amount) {
        this.count = this.count - amount
      }
    },
  }
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
