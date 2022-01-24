<template>
    <div>
        <p>Descrição da pessoa: {{ name }}</p>
        <info />

    </div>
</template>
<script>
    import Info from './Info.vue'

    export default {
        name: 'Pessoa',
        components:{
            Info,
        }, 
        data() {
            return {
                name: 'Gabriel'
            }
        }
    }
</script>