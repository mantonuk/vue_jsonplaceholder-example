<template>
  <div id="app">
    <PageHeader somePropsValue="somePropsValue Header"/>
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/>-->
    <Posts title="Posts" />
    <PageFooter somePropsValue="somePropsValue Footer"/>
  </div>
</template>

<script>
import PageHeader from './components/PageHeader.vue'
import Posts from './components/Posts.vue'
import PageFooter from './components/PageFooter.vue'
/*import HelloWorld from './components/HelloWorld.vue'*/

export default {
  name: 'App',
  components: {
    PageHeader,
    Posts,
    PageFooter,
    /*HelloWorld*/
  }
}
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
