<template>
    <div>
        <Header />
        <Comp-1 />
        <Lifecycle />
        <Pessoa />
    </div>
</template>

<script>
    import Comp1 from './components/Comp1.vue'
    import Header from './components/Header.vue'
    import Lifecycle from './components/Lifecycle.vue'
    import Pessoa from './components/Pessoa.vue'

    export default {
        name: 'App',
        components: {
            Header,
            Comp1,
            Lifecycle,
            Pessoa
        },  
    }
</script>

<style>
    body {
        font-family: Arial, Helvetica, sans-serif;
        background-color: #333;
        color: #fff;
    }
    a {
        color: lightblue;
    }
</style>