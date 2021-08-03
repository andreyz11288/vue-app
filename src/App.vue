<template>
  <div id="app">
    <ApartmentsItem
      :descr="apartments.descr"
      :rating="apartments.rating"
      :price="apartments.price"
      imgSrc="https://miro.medium.com/max/2000/1*cLQUX8jM2bMdwMcV2yXWYA.jpeg"
    />
  </div>
</template>

<script>
import ApartmentsItem from './components/Apartments/ApartmentsItem.vue'

export default {
  name: 'App',
  components: {
    ApartmentsItem,
  },
  data() {
    return {
      apartments: {
        id: '1jh144',
        title: 'Aut qui jgjkhgfgf jhhghfg ggggcc',
        descr:
          'kilhgkuhuf ,kjkhguyhugf lkiujhhguy jhlijggi kijbjh jugjuuhbg jhigiugivg ijhugi ijugiiuiuu jh ijhghvhg kijj iouib ijb kijh nbvhvg',
        rating: 3.5,
        price: 2032,
        locftion: {
          city: 'Kherson',
        },
        owner: {
          name: 'Ellen',
          phone: '115-355-5652',
          email: 'xegfrf,hf',
        },
      },
    }
  },
}
</script>

<style>
#app {
  font-family: Montserrat, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
