<template>
    <section className="categories-list">
        <div v-for="(icon, index) in iconList" :key="'item-'+index" class="categories-list__item">
                <Icon :data="icon" />
        </div>
    </section>
</template>

<script>
import Icon from "./Icon";

export default {
    name: 'CategoriesList',
    components: {
        Icon
    },
    props: {
        iconList: [Object]
    }
}
</script>

<style lang="stylus" scoped>
.categories-list
    padding 0 20px
    width 100%
    box-sizing border-box
    display flex
    justify-content center
    overflow auto
    color #44535B
    .categories-list__item 
        padding 0 20px

</style>