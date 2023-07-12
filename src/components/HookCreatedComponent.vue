<template>
    <div id="HookCreatedComponent">
        <ul>
            <li v-for='character in characters' :key="character.id">
                {{ character.name }}
            </li>
        </ul>
    </div>
</template>

<script>
import axios from 'axios';
export default{
    name:'HookCreatedComponent',
    data: function(){
        return{
            characters:[],
        }
    },
    methods:{

    },
    computed:{

    },
    created(){
        let url = 'https://rickandmortyapi.com/api/character';

        axios.get(url)
            .then(resp =>{
                console.log(resp);
                this.characters = resp.data.results;
            })
            .catch(err=>{
                console.log(err);
            });
    }

}
</script>

<style scoped>
#HookCreatedComponent{
    background-color: aquamarine;
}
</style>