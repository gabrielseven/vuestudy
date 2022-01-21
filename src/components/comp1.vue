<template>
    <div>    
        <h1>Olá Vue!</h1>
        <p>Nome é {{ nome }} e estou no {{ clube }}</p>
    </div>

</template>

<script>
    export default {
        name: 'comp1',
        data(){
            return {
                nome: "Gabriel",
                clube: "Charrete Esporte"
            }

        }    
    }
</script>