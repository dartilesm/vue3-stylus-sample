<template>
    <div className="icon">
        <img :src="data.icon" alt="supermercado" class="icon__icon" />
        <span v-if="data.text" v-text="data.text" :class="['icon__name', data.selected && 'icon__name--selected']"></span>
    </div>
</template>

<script>
export default {
    name: 'Icon',
    props: {
        data: {
            icon: String,
            text: String,
            selected: Boolean
        }
    }
}
</script>

<style lang="stylus" scoped>
.icon
    display flex
    cursor pointer
    flex-direction column
    justify-content center
    align-items center
    .icon__name
        white-space nowrap
        overflow hidden
        text-overflow ellipsis
    .icon__name--selected
        color #00AF71
</style>