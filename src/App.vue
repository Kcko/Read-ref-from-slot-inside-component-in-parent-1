<template>
  <div id="app">
    <HelloWorld name="child" :b="setRefOnA">
      <input type="text" ref="a" value="default value of this input" />
    </HelloWorld>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
  },
  methods: {
    setRefOnA(el) {
      return this.$refs.a;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
