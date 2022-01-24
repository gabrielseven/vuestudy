<template>
    <div>
        <p v-if="currentlyWorking">Estou trabalhando no momento.</p>
        <p v-else style="color: red;">Não estou trabalhando no momento.</p>
        <p>Utilizo as seguintes tecnologias:</p>
        <ul>
            <li>JavaScript</li>
            <li>PHP</li>
            <li>Python</li>
            <li>Delphi</li>
        </ul>
        <p>Para acessar meu portfólio, <a v-bind:href="portfolioLink" target="_blank">basta clicar aqui</a></p>
        <Picture />
    </div>
</template>

<script>
    import Picture from './picture.vue'

    export default {
        name: 'Info',
        components: {
            Picture
        },
        data() {
            return {
                currentlyWorking: false,
                portfolioLink: 'https://google.com'
            }
        }
    }
</script>