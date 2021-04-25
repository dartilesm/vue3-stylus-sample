

const LEFT_ICON_LIST = [
    {
        icon: StoreIcon,
        padding: true,
        text: 'Tiendas',
        selected: true
    },
    {
        icon: LocationIcon,
        padding: true,
        text: 'Caracas'
    }
]

const CENTERED_ICON = {
    icon: CartIcon,
    roundedShadow: true
}

const RIGHT_ICON_LIST = [
    {
        icon: MoneyIcon,
        padding: true,
        text: 'Gana $5.00'
    },
    {
        icon: UserIcon,
        padding: true,
        text: 'Iniciar Sesión'
    }
]


<template>
    <footer className="footer">
        <div className="footer__icon-center">
            <div className="footer__icon-center-container">
                <Icon :data="icons.centeredIconList" />
            </div>
        </div>
        <div className="footer__container">
            <div className="footer__icon-left">
                <Icon v-for="(data, index) in icons.leftIconList" :data="data" :key="'leftIcon-'+index" />
            </div>
            <div className="footer__icon-right">
                <Icon v-for="(data, index) in icons.rightIconList" :data="data" :key="'rightIcon-'+index" />
            </div>
        </div>
</footer>
</template>

<script>
import CartIcon from '../assets/footer/cart.svg'
import StoreIcon from '../assets/footer/store.png'
import LocationIcon from '../assets/footer/location.svg'
import MoneyIcon from '../assets/footer/money.svg'
import UserIcon from '../assets/footer/user.svg'
import Icon from './Icon'

const LEFT_ICON_LIST = [
    {
        icon: StoreIcon,
        padding: true,
        text: 'Tiendas',
        selected: true
    },
    {
        icon: LocationIcon,
        padding: true,
        text: 'Caracas'
    }
]

const CENTERED_ICON = {
    icon: CartIcon,
    roundedShadow: true
}

const RIGHT_ICON_LIST = [
    {
        icon: MoneyIcon,
        padding: true,
        text: 'Gana $5.00'
    },
    {
        icon: UserIcon,
        padding: true,
        text: 'Iniciar Sesión'
    }
]

export default {
    name: 'Footer',
    components: {
        Icon
    },
    data() {
        return {
            cartIcon: CartIcon,
            storeIcon: StoreIcon,
            locationIcon: LocationIcon,
            moneyIcon: MoneyIcon,
            userIcon: UserIcon,
            icons: {
                leftIconList: LEFT_ICON_LIST,
                centeredIconList: CENTERED_ICON,
                rightIconList: RIGHT_ICON_LIST
            }
        }
    }
}
</script>

<style lang="stylus" scoped>
.footer
    position relative
    height 86px
    width 100%
    color #44535B
    .footer__container
        position absolute
        bottom 0
        height calc(100% - 10px)
        width 100%
        display flex
        justify-content space-between
        overflow hidden
        background #FFFFFF
        border-radius 20px 20px 0 0
        box-shadow 0px -2px 4px rgba(140, 162, 174, 0.2)
        .footer__icon-left, .footer__icon-right
            display inline-flex
            width 40%
            justify-content space-around
    .footer__icon-center
        top -5px
        width 20%
        position absolute
        left 50%
        transform translateX(-50%)
        display flex
        justify-content center
        z-index 1
        .footer__icon-center-container 
            padding 20px
            border-radius 20px
            background-color white
            box-shadow 2px 2px 10px rgba(140, 162, 174, 0.2)
</style>