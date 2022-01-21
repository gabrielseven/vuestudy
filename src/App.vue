<template>
    <div>
        <comp1 />
        <lifecycle />
        <pessoa />
    </div>
</template>

<script>
    import comp1 from './components/comp1.vue'
    import lifecycle from './components/lifecycle.vue'
    import pessoa from './components/pessoa.vue'

    export default {
        name: 'App',
        components: {
            comp1,
            lifecycle,
            pessoa
        }    
    }
</script>
