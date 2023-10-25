<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <DeclarativeRendering/>
  <AttributeBinding/>
  <EventListener/>
  <FormBindings/>
  <ConditionalRendering/>
  <ListRendering/>

</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import DeclarativeRendering from './components/DeclarativeRendering.vue';
import AttributeBinding from './components/AttributeBinding.vue';
import EventListener from './components/EventListener.vue';
import FormBindings from './components/FormBindings.vue';
import ConditionalRendering from './components/ConditionalRendering.vue';
import ListRendering from './components/ListRendering.vue';
export default {
  name: 'App',
  components: {
    // HelloWorld
    DeclarativeRendering,
    AttributeBinding,
    EventListener,
    FormBindings,
    ConditionalRendering,
    ListRendering
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
