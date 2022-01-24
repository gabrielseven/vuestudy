<template>
    <div>
        <div>
            <button @click="toggleJob">Mudar status</button>
        </div>
        <p v-if="currently_working" style="color: lightgreen;">Estou trabalhando no momento.</p>
        <p v-else style="color: red;">Não estou trabalhando no momento.</p>
        <p>Tecnologias back-end:</p>
        <ul>
            <li v-for="(technology, index) in back_technologies" v-bind:key="index">
                {{ technology }}
            </li>
        </ul>
        <p>Tecnologias front-end:</p>
        <ul>
            <li v-for="technology in front_technologies" :key="technology.id">
                {{ technology.language }}
            </li>
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
    import Picture from './Picture.vue'

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
                portfolio_link: 'https://google.com',
                back_technologies: ['JavaScript', 'PHP', 'Python', 'Delphi'],
                front_technologies: [
                    {id:1, language: 'HTML' },
                    {id:2, language: 'CSS' },
                    {id:3, language: 'Vue' },
                    {id:4, language: 'React' }
                ]
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
            },
            toggleJob () {
                this.currently_working = !this.currently_working
            }
        }
    }
</script>