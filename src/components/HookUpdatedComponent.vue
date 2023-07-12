<template>
    <div id="HookUpdatedComponent">
        <h1>{{ number }}</h1>
        <button v-on:click="sumar">Incrementar</button>
    </div>
</template>

<script>
export default{
    name:'HookUpdatedComponent',
    data:function(){
        return{
            number: 0,
        }
    },
    methods:{
        sumar:function(){
            this.number+=1;
        }
    },
    computed:{

    },
    beforeUpdate(){
        console.log('hook beforeUpdate');
        alert(this.number);
    },
    updated(){
        console.log('hook updated');
        console.log(this.number);
    }
}
</script>

<style scoped>
#HookUpdatedComponent{
    background-color: darksalmon;
}
</style>