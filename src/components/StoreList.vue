<template>
    <section class="stores-list">
        <StoreCard v-for="(store, index) in stores" :key="'store-'+index" v-bind="store" />
    </section>
</template>

<script>
import StoreCard from "./StoreCard";

export default {
    name: 'StoreList',
    components: {
        StoreCard
    },
    props: {
        stores: Array
    }
}
</script>

<style lang="stylus" scoped>
.stores-list
    display flex
    padding 30px 20px
    box-sizing border-box
    flex-wrap wrap
    justify-content center
</style>