<script>
import AppLogo from './AppLogo.vue';

export default {
    name: 'AppHeader',
    components: {
        AppLogo
    },
    data() {
        return {

            links: [
                {
                    label: 'Home',
                    url: '#',
                    active: false
                },
                {
                    label: 'Prodotti',
                    url: '#',
                    active: true
                },
                {
                    label: 'Chi Siamo',
                    url: '#',
                    active: false
                },
                {
                    label: 'Contatti',
                    url: '#',
                    active: false
                }
            ]

        };
    }
}
</script>

<template>

    <header>

        <div>
            <AppLogo />
        </div>

        <ul>
            <li v-for="link in links">
                <a :href="link.url" :class="{
                    active: link.active == true
                }">
                    {{ link.label }}
                </a>
            </li>
        </ul>

    </header>

</template>

<style lang="scss" scoped>
div {
    text-align: center;
}

header {
    padding-bottom: 50px;
}

ul {
    display: flex;
    justify-content: center;
    list-style: none;

    li {
        a {
            display: inline-block;
            padding: 15px;
            font-weight: bold;
            text-decoration: none;
            color: black;

            &.active {
                background-color: #DAE9FE;
            }
        }
    }
}
</style>