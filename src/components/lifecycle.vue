<template>
    <h1> {{ nome }}</h1>
</template>

<script>
    export default {
        name: 'lifecycle',
        data() {
            return{
                nome: 'Tabela'
            }
        },
        created(){
            setTimeout (() => {
                this.nome = 'Química Mix x Pão de Alho'
            }, 2000);
            this.lifeCycleEvent()
        },
        mounted(){
            setTimeout (() => {
                this.nome = 'Final FutSoftware 2014'
            }, 4000);
            this.lifeCycleEvent()

        },
        methods: {
            lifeCycleEvent() {
                
            }
        }
    }
</script>
