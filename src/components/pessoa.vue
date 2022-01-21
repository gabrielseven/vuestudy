<template>
    <div>
        <p>Descrição da pessoa: {{ name }}</p>
        <info />
        <alho />

    </div>
</template>
<script>
    import info from './info.vue'
    import alho from './alho.vue'

    export default {
        name: 'Pessoa',
        components:{
            info,
            alho
        }, 
        data() {
            return {
                name: 'Gabriel'
            }
        }
    }
</script>