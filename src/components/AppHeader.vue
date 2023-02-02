<script>
import AppLogo from './AppLogo.vue';

export default {
    name: 'AppHeader',
    components: {
        AppLogo
    }
}
</script>

<template>

    <header>

        <div>
            <AppLogo />
        </div>

        <ul>
            <li>
                <a href="#">
                    Home
                </a>
            </li>
            <li>
                <a href="#" class="active">
                    Prodotti
                </a>
            </li>
            <li>
                <a href="#">
                    Chi Siamo
                </a>
            </li>
            <li>
                <a href="#">
                    Contatti
                </a>
            </li>
        </ul>

    </header>

</template>

<style lang="scss" scoped>
div {
    text-align: center;
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