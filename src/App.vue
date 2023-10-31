<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <DeclarativeRendering/>
  <AttributeBinding/>
  <EventListener/>
  <FormBindings/>
  <ConditionalRendering/>
  <ListRendering/>
  <LifecycleAndTemplateRef/>
  <WatcherInit/>
  <PropsInit msg="greeting"/>
  <EmitsInit @responseEmit="responseEmit"/>
  <h2>{{ msg }}</h2>
  <SlotInit><h3>masssge from parent : {{ msg }}</h3></SlotInit>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import DeclarativeRendering from './components/DeclarativeRendering.vue';
import AttributeBinding from './components/AttributeBinding.vue';
import EventListener from './components/EventListener.vue';
import FormBindings from './components/FormBindings.vue';
import ConditionalRendering from './components/ConditionalRendering.vue';
import ListRendering from './components/ListRendering.vue';
import LifecycleAndTemplateRef from './components/LifecycleAndTemplateRef.vue';
import WatcherInit from './components/WatcherInit.vue';
import PropsInit from './components/PropsInit.vue';
import EmitsInit from './components/EmitsInit.vue';
import SlotInit from './components/SlotInit.vue';
import { ref } from 'vue';
export default {

  name: 'App',
  components: {
    // HelloWorld
    DeclarativeRendering,
    AttributeBinding,
    EventListener,
    FormBindings,
    ConditionalRendering,
    ListRendering,
    LifecycleAndTemplateRef,
    WatcherInit,
    PropsInit,
    EmitsInit,
    SlotInit
  },
  setup(){
    const msg = ref('Waiting Emit..!');
    const responseEmit = (newMsg) =>{
      msg.value = newMsg
    }
    return {
      msg, 
      responseEmit
    }
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
