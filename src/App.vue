<template>
  <div id="app">
    <ApartmentsList :items="apartments" />
  </div>
</template>

<script>
import ApartmentsList from './components/Apartments/ApartmentsList.vue'

export default {
  name: 'App',
  components: {
    ApartmentsList,
  },
  data() {
    return {
      apartments: [
        {
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
          imgUrl:
            'https://miro.medium.com/max/2000/1*cLQUX8jM2bMdwMcV2yXWYA.jpeg',
        },
        {
          id: '1jh174',
          title: 'dfb fthth rth rAut qui jgjkhgfgf jhhghfg ggggcc',
          descr:
            'rth rth rt th rth kilhgkuhuf ,kjkhguyhugf lkiujhhguy jhlijggi kijbjh jugjuuhbg jhigiugivg ijhugi ijugiiuiuu jh ijhghvhg kijj iouib ijb kijh nbvhvg kjbkjhbv ljkjhvku lihvkuhvuki ljihvkubiukv lkjhvu k,jhg   kulvguibibi lihvb lijb',
          rating: 4.5,
          price: 2072,
          locftion: {
            city: 'Kherson',
          },
          owner: {
            name: 'Ellen',
            phone: '115-355-5652',
            email: 'xegfrf,hf',
          },
          imgUrl:
            'https://miro.medium.com/max/2000/1*cLQUX8jM2bMdwMcV2yXWYA.jpeg',
        },
      ],
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
