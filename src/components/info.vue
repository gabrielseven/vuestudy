<template>
    <div>
        <p v-if="currently_working">Estou trabalhando no momento.</p>
        <p v-else style="color: red;">Não estou trabalhando no momento.</p>
        <p>Utilizo as seguintes tecnologias:</p>
        <ul>
            <li>JavaScript</li>
            <li>PHP</li>
            <li>Python</li>
            <li>Delphi</li>
        </ul>
        <div>
            <button @click="toggleEmail">{{ button_text }}</button>
        </div>
        <p v-show="show_email">{{ email }}</p>
        <p>Para acessar meu portfólio, <a v-bind:href="portfolio_link" target="_blank">basta clicar aqui</a></p>
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
                currently_working: false,
                email: "gabrielteste@email.com",
                show_email: false,
                button_text: 'Mostrar e-mail',
                portfolio_link: 'https://google.com'
            }
        },
        methods: {
            toggleEmail() {
                this.show_email = !this.show_email
                if (!this.show_email) {
                    this.button_text = 'Mostrar e-mail'
                } else {
                    this.button_text = 'Ocultar e-mail'
                }
            }
        }
    }
</script>