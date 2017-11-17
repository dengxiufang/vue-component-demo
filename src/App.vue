<template>
  <div id="app">
      <child v-on:listenToChildEvent="showMsgFromChild" v-bind:message="parentMsg"></child>
  </div>
</template>

<script>
import child from './components/Child'
export default {
  name: 'app',
  data () {
    return {
        parentMsg: 'hello word'
    }
  },
  components: {
      child
  },
  methods: {
    showMsgFromChild (data) {
        console.log(data);
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
