<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <LifeCycleComponente />
  <hr>
  <HookCreatedComponent />
  <hr>
  <HookMountedComponent />
  <hr>
  <HookUpdatedComponent />
  <hr>
  <div v-if="mostrar">
    <HookDestroyedComponent />
  </div>
  <button v-on:click="mostrar=true">Mostrar</button><button v-on:click="mostrar=false">No Mostrar</button>

</template>

<script>

import LifeCycleComponente from '@/components/LifeCycleComponente.vue';
import HookCreatedComponent from '@/components/HookCreatedComponent.vue';
import HookMountedComponent from '@/components/HookMountedComponent.vue';
import HookUpdatedComponent from '@/components/HookUpdatedComponent.vue';
import HookDestroyedComponent from '@/components/HookDestroyedComponent.vue';
export default {
  name: 'App',
  components: {
    LifeCycleComponente,
    HookCreatedComponent,
    HookMountedComponent,
    HookUpdatedComponent,
    HookDestroyedComponent,
  },
  data:function(){
    return{
      mostrar:true,
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
