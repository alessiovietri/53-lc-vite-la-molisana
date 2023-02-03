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

        <div class="container">

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

        </div>

    </footer>

</template>

<style lang="scss" scoped>

.container {
    @include container;

    > * {
        width: calc(100% / 3);

        img {
            max-width: 100%;
        }

        h3 {
            text-transform: uppercase;
            color: $main-blue;
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

footer {
    @include bg('../assets/img/footer-montagne-bottom.jpg', center bottom, 100% auto);

    padding: 20px 0 150px;
}

</style>