<template>
    <header class="header">
        <div class="header__logo-container">
            <img src="../assets/logo.png" alt="logo" class="header__logo" />
        </div>
        <div class="header__banner-text-container">
            <p class="header__banner-text">Envía bienestar a tu familia en <b class="header__banner-text-bold">Argentina</b></p>
        </div>
        <div class="header__banner-image-container">
        </div>
        <div class="header__search-container">
            <SearchField placeholder="¿Qué estás buscando?"/>
        </div>
    </header>
</template>

<script>
import SearchField from './SearchField'

export default {
    name: 'Header',
    components: {
        SearchField
    }
}
</script>

<style lang="stylus" scoped>
.header
    position relative
    border-radius 0 0 20px 20px
    background linear-gradient(89.41deg, #0DBA72 2.6%, #0DBA72 99.38%)
    min-width 375px
    width 100%
    height 188px
    .header__logo-container
        margin 26px 20px
        display inline-block
    .header__banner-text-container
        position relative
        width 80%
        padding 0 20px
        font-size 1.5em
        box-sizing border-box
        z-index 1
    .header__banner-text
        color white
    .header__banner-text-bold
        color white
    .header__banner-image-container
        position absolute
        width 100%
        height 80%
        overflow hidden
        bottom 0
        border-radius 0 0 20px 20px
        background-image url(../assets/banner.png)
        background-size contain
        background-repeat no-repeat
        background-position right
    .header__banner-image
        position absolute
        right 0
        height 100%
        object-fit contain
    .header__search-container 
        position absolute
        left 50%
        transform translateX(-50%)
        width 80%
        bottom -20px
</style>
