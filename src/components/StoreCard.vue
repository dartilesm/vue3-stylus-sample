<template>
    <div class="store-card store-card--margin-15">
        <div class="store-card__container">
            <div :class="['store-card__header', `store-card__header--${store}`]">
                <span v-if="discount" class="store-card__discount" v-text="`Hasta ${discount}% dto.`"></span>
            </div>
            <div class="store-card__body">
                <h4 class="store-card__title" v-text="title"></h4>
                <p class="store-card__category">
                    {{category}}
                    <span class="store-card__stars-container">
                        <img class="store-card__start-icon" :src="starIcon" alt="star" />
                        {{stars}}
                    </span>
                </p>
            <p class="store-card__delivery-info">
                <img class="store-card__delivery-icon" :src="deliveryIcon" alt="truck delivery" />
                {{`${deliveryTime} • Gasta $ 80.0000 para envio GRATIS`}}
            </p>
            </div>
        </div>
        <div class="store-card__badge">
            <span class="store-card__badge-text">
                Delivery
            </span>
        </div>
    </div>
</template>


<script>
import StarIcon from '../assets/star.png'
import DeliveryIcon from '../assets/delivery.svg'

export default {
    name: 'StoreCard',
    props: {
        store: String,
        title: String,
        discount: String,
        category: String,
        stars: String,
        deliveryTime: String
    },
    data() {
        return {
            starIcon: StarIcon,
            deliveryIcon: DeliveryIcon
        }
    }
}
</script>


<style lang="stylus" scoped>
.store-card
    position relative
    cursor pointer
    max-width 331px
    width 100%
    height 231px
    z-index 1
    color #44535B
    &.store-card--margin-15
        margin 15px
    &::before
        content ''
        position absolute
        width 66px
        height 24px
        border-radius 10px
        background-color white
        bottom -8px
        right 15px
        z-index -1
        box-shadow 0px 2px 4px rgba(140, 162, 174, .2)
    .store-card__container
        height calc(100% - 10px)
        width 100%
        background-color white
        box-shadow 0px 2px 4px rgba(140, 162, 174, .2)
        border-radius 20px
    .store-card__header
        position relative
        border-radius 20px 20px 0 0
        width 100%
        height 142px
    .store-card__header--delicateck
        background-image url('../assets/stores/delicateck.png')
    .store-card__header--lomas
        background-image url('../assets/stores/lomas.png')
    .store-card__discount
        position absolute
        right 0
        background-color #FFC431
        padding 7px 13px
        border-radius 0 12px 0 12px
        text-transform uppercase
        font-weight 600
        font-size .7em
    .store-card__body
        padding 9px 25px 18px 25px
    .store-card__category
        font-size .8em
    .store-card__delivery-info
        font-size .7em
    .store-card__badge
        display inline-flex
        justify-content center
        align-items center
        position absolute
        width 66px
        height 24px
        bottom -8px
        right 15px
        border-radius 10px
        background-color white
    .store-card__badge-text
        background: #00AF71;
        border-radius: 6px;
        padding: 0px 5px;
        color: white;
        font-size: .6em;
        text-transform uppercase
</style>