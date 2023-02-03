<script>

export default {
    name: 'CardElement',
    // Dati dall'esterno
    props: {
        title: String,
        src: String
    },
    // Dati interni
    data() {
        return {
            message: 'Ciao'
        };
    }
}

</script>

<template>
    <div class="card">

        <div>
            <img :src="src" :alt="title">
        </div>

        <h4>
            {{ title }}
        </h4>

        <p>
            {{ message }}
        </p>

    </div>
</template>

<style lang="scss" scoped>
.card {
    img {
        width: 100%;
    }
}
</style>