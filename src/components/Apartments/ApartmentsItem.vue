<template>
  <li class="apartments-item" @click="log">
    <div class="apartments-item__inner">
      <img :src="imgSrc" alt="" class="apartments-item__photo" />
      <div class="apartments-item__content" >
        <p class="apartments-item__description">{{ descr }}</p>
        <div class="apartments-item__rating">
          <StarRating :rating="rating" />
        </div>
        <div class="apartments-item__price">UAH {{ price }}</div>
      </div>
    </div>
  </li>
</template>

<script>
import StarRating from '../StarRating.vue'

export default {
  name: 'ApartmentsItem',
  components: {
    StarRating,
  },
  props: {
    descr: {
      type: String,
      default: '',
    },
    rating: {
      type: Number,
      default: 0,
    },
    price: {
      type: Number,
      require,
    },
    imgSrc: {
      type: String,
      default: 'https://miro.medium.com/max/2000/1*cLQUX8jM2bMdwMcV2yXWYA.jpeg',
    },
  },
  methods:{
    log(event){
      console.log(event);
    }
  }
}
</script>

<style lang="scss" scoped>
.apartments-item {
  position: relative;
  max-width: 350px;
  padding: 0 20px;

  &__inner {
    position: relative;
  }

  &__content {
    position: relative;
    padding: 20px;
    opacity: 0;
    transition: opacity 0.4s;
    background: rgba(#0f1d2d, 0.7);
    min-height: 200px;
    color: #fff;
    text-align: left;
    line-height: 1.4;
    cursor: pointer;
    z-index: 1;

    &:hover {
      opacity: 1;
    }
  }
  &__description {
    margin-bottom: 20px;
    height: calc(1em * 1.4 * 5);
    overflow: hidden;
  }

  &__rating {
    margin-bottom: 20px;
  }

  &__price {
    font-size: 20px;
    font-weight: 600;
  }
  &__photo {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
}
</style>
