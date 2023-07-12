<template>
    <div id="HookDestroyedComponent">
        <h1>Componente HookDestroyed</h1>
        <button v-on:click="desmontar">Desmontar componente</button>
    </div>
</template>

<script>
export default{
    name: 'HookDestroyedComponent',
    data:function(){
        return{

        }
    },
    methods:{
        desmontar:function(){
            console.log('Llamada a funcion desmontar');
        },  
    },
    computed:{},
    beforeMount(){
        console.log('beforeMount');
        alert('beforeMount');
    },
    mounted(){
        console.log('mounted');
    },
    beforeUnmount(){
        console.log('beforeUnmount');
        alert('beforeUnmount');
    },
    unmounted(){
        console.log('unmounted');
    }


}
</script>

<style scoped>
#HookDestroyedComponent{
    background-color: brown;
}
</style>