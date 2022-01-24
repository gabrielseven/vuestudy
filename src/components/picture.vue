<template>
    <img :src="avatar" :alt="descricao" width="200" height="200">
</template>
<script>
    export default {
        name: 'Picture',
        data() {
            return {
                avatar: "/img/avatar.png",
                descricao: "Nome do Usuário"
            }
        }
    }
</script>