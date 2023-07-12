<template>
    <div id="HookMountedComponent">
        <Bar id="my-chart-id"
            v-bind:options="chartOptions"
            v-bind:data="chartData"
        />
        <p id="saludar">{{ saludo }}</p>
        <p id="saludar2"></p>
    </div>
</template>

<script>
import { Bar } from 'vue-chartjs';
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale } from 'chart.js';
ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale);

export default{
    name:'HookMountedComponent',
    components:{
        Bar,
    },
    data: function(){
        return{
            chartOptions:{
                responsive:true,
            },
            chartData:{
                labels:['Abril','Mayo','Junio'],
                datasets:[{
                    label: 'ventas',
                    data:[130,10,80],
                        }],
            },
            saludo:'',
        }
    },
    methods:{

    },
    computed:{

    },

    mounted(){
        console.log('mounted');
        
            this.saludo='Hola Mundo !!!!';
            let elParrafo2 = document.getElementById('saludar2');
            elParrafo2.innerText = ' Adios Mundo';
        
    }


}
</script>

<style scoped>
   #HookMountedComponent{
    border: 1px solid blue;
    width: 60%;
    margin: 0 auto;
   } 

   #saludar{
    background-color: blueviolet;
    color: white;
   }

   #saludar2{
    background-color: red;
    color: yellow;
   }
</style>