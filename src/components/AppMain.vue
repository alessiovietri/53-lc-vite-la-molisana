<script>
import CardElement from './CardElement.vue';

export default {
    name: 'AppMain',
    components: {
        CardElement
    },
    data() {
        return {
            products: [
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/1-spaghetto-quadrato.jpg",
                    titolo: "N.4 Spaghetto Quadrato Bucato",
                    tipo: "lunga",
                    cottura: 6,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/5-fettuccine.jpg",
                    titolo: "N.5 Fettuccine",
                    tipo: "lunga",
                    cottura: 13,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/6-linguine.jpg",
                    titolo: "N.6 Linguine",
                    tipo: "lunga",
                    cottura: 12,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/7-mezze-linguine.jpg",
                    titolo: "N.7 Mezze Linguine",
                    tipo: "lunga",
                    cottura: 11,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/11-spaghettino-quadrato.jpg",
                    titolo: "n.11 Spaghettino Quadrato",
                    tipo: "lunga",
                    cottura: 9,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/38-mezze-maniche.jpg",
                    titolo: "N.38 Mezze maniche",
                    tipo: "corta",
                    cottura: 12,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/44-sedani.jpg",
                    titolo: "N.44 Sedani",
                    tipo: "corta",
                    cottura: 8,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/49-sedani.jpg",
                    titolo: "N.49 Sedanini",
                    tipo: "corta",
                    cottura: 8,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/53-lumachine.jpg",
                    titolo: "N.53 Lumachine",
                    tipo: "corta",
                    cottura: 12,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/55-chifferi-rigati.jpg",
                    titolo: "N.55 Chifferi rigati",
                    tipo: "corta",
                    cottura: 12,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/58-misto-corto.jpg",
                    titolo: "N.58 Misto corto",
                    tipo: "corta",
                    cottura: 9,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/06/84-ditale-quadrato.jpg",
                    titolo: "N.84 Ditale Quadrato",
                    tipo: "cortissima",
                    cottura: 12,
                },
            ],
            onSale: [
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/1-spaghetto-quadrato.jpg",
                    titolo: "N.4 Spaghetto Quadrato Bucato",
                    tipo: "lunga",
                    cottura: 6,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/5-fettuccine.jpg",
                    titolo: "N.5 Fettuccine",
                    tipo: "lunga",
                    cottura: 13,
                },
            ]
        };
    }
}

</script>

<template>

    <main>

        <div class="container">
            <div>
                <h1>
                    Lista prodotti
                </h1>

                <div class="products">
                    <CardElement v-for="product in products" 
                        class="product"
                        :title="product.titolo"
                        :src="product.src" />
                </div>

                <hr>

                <h2>
                    Prodotti in offerta
                </h2>

                <div class="products">
                    <CardElement v-for="product in onSale"
                        class="product on-sale"
                        :title="product.titolo"
                        :src="product.src" />
                </div>
            </div>
        </div>

    </main>

</template>

<style lang="scss" scoped>

main {
    @include bg('../assets/img/fondo-pag-speciali.jpg');

    padding: 50px 0;
}

hr {
    margin: 40px 0;
}

h1, h2 {
    color: $main-blue;
    text-align: center;
}

.container {
    @include container;

    color: $main-blue;
    justify-content: center;
    font-size: 1.5rem;
    font-weight: bold;
}

.products {
    display: flex;
    flex-wrap: wrap;

    .product {
        width: 25%;
        background-color: white;
        padding: 20px;
        text-align: center;
        border: 2px solid lavender;

        &.on-sale {
            width: 50%;
            background-color: lightseagreen;
        }
    }
}
</style>