<template>
    <div id="LifeCycleComponente">

    </div>
</template>


<script>
export default{
    name:'LifeCycleComponente',
    data:function(){
        return{
            number:0,
        }
    },
    methods:{

    },
    computed:{

    },
    beforeCreate(){
        console.log(this);
        console.log(this.number);
    }

}
</script>