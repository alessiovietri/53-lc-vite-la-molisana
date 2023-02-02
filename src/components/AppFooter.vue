<script>
import AppLogo from './AppLogo.vue';

export default {
    name: 'AppFooter',
    components: {
        AppLogo
    }
}
</script>

<template>

    <footer>

        <div>
            <AppLogo />
        </div>

        <div>
            <h3>
                Pastificio
            </h3>
            <ul>
                <li>
                    <a href="#">
                        Link 1
                    </a>
                </li>
                <li>
                    <a href="#">
                        Link 2
                    </a>
                </li>
                <li>
                    <a href="#">
                        Link 3
                    </a>
                </li>
                <li>
                    <a href="#">
                        Link 4
                    </a>
                </li>
            </ul>
        </div>

        <div>
            <h3>
                Prodotti
            </h3>
            <ul>
                <li>
                    <a href="#">
                        Link 1
                    </a>
                </li>
                <li>
                    <a href="#">
                        Link 2
                    </a>
                </li>
                <li>
                    <a href="#">
                        Link 3
                    </a>
                </li>
                <li>
                    <a href="#">
                        Link 4
                    </a>
                </li>
            </ul>
        </div>

    </footer>

</template>

<style lang="scss" scoped>

footer {
    display: flex;
    max-width: 1000px;
    margin: 0 auto;

    > * {
        width: calc(100% / 3);

        img {
            max-width: 100%;
        }

        h3 {
            text-transform: uppercase;
            color: blue;
            margin-bottom: 25px;
        }

        ul {
            list-style: none;

            li {
                a {
                    display: inline-block;
                    padding: 5px 15px;
                    text-decoration: none;
                    color: black;
                }
            }
        }
    }
}

</style>