<template>
  <Header />
  <StoreLocation location="Caracas, Ajuro" />
  <CategoriesList :iconList="iconList" />
  <StoreList :stores="storeList" />
  <Footer />
</template>

<script>
import Header from './components/Header';
import CategoriesList from './components/CategoriesList';
import StoreLocation from './components/StoreLocation';
import StoreList from './components/StoreList';
import Footer from './components/Footer';
import MarketIcon from './assets/categories/super.png'
import ButcherShopIcon from './assets/categories/carniceria.png'
import PharmaIcon from './assets/categories/pharma.png'

const ICON_LIST = [
  {
    icon: MarketIcon,
    text: 'Supermercado',
    selected: true,
    padding: true
  },
  {
    icon: ButcherShopIcon,
    text: 'Carnicería',
    selected: false,
    padding: true
  },
  {
    icon: PharmaIcon,
    text: 'Farmacia',
    selected: false,
    padding: true
  }
]

const STORE_LIST = [
  {
    store: 'delicateck',
    discount: 20,
    title: 'Delicateck Caracas',
    category: 'Supermercado',
    stars: '4.5',
    deliveryTime: '3 días'
  },
  {
    store: 'lomas',
    discount: 20,
    title: 'Lomas Supermercado',
    category: 'Supermercado',
    stars: '4.5',
    deliveryTime: '3 días'
  }
]

export default {
  name: 'App',
  components: {
    Header,
    CategoriesList,
    StoreLocation,
    StoreList,
    Footer
  },
  data() {
    return {
      iconList: ICON_LIST,
      storeList: STORE_LIST
    }
  }
}
</script>

<style lang="stylus">
*
    margin 0
    font-family 'Poppins', sans-serif
</style>