<template>
    <div class="v-main-wrapper">
        <p>{{title}}</p>
        <v-catalog></v-catalog>
        <v-cart></v-cart>
    </div>
</template>

<script>
    import vCatalog from './v-catalog'
    import vCart from './v-cart'

    export default {
        name: 'v-main-wrapper',
        components: {
            vCatalog,
            vCart
        }, //дочерние компоненты
        props: {}, //то что прилетает из родителя
        data() { //данные для текущего компонента
            return {
                title: 'Main Wrapper'
            }
        },
        computed: {}, //вычисляемые свойства
        methods: {}, //клики анимации и тд
        watch: {}, //следить за чем либо
        mounted() { //когда компонент загрузится
            console.log("v-main-wrapper is loaded!");
        }
    }
</script>

<style>
    .v-main-wrapper {
        display: flex;
        justify-content: center;
        align-items: center;
        max-width: 900px;
        margin: 0 auto;
    }
</style>