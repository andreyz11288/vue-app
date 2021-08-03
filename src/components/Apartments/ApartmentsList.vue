<template>
  <Container>
    <ul class="apartments-list">
      <template v-for="apartment in items">
        <slot name="apartment" v-bind:apartment="apartment"></slot>
      </template>
    </ul>
  </Container>
</template>

<script>
// import ApartmentsItem from './ApartmentsItem.vue'
import Container from '../shared/Container.vue'

export default {
  name: 'ApartmentsList',
  components: {
    // ApartmentsItem,
    Container,
  },
  props: {
    items: {
      type: Array,
      default: () => [],
    },
  },
}
</script>

<style lang="scss" scoped>
.apartments-list {
  display: flex;
  flex-wrap: wrap;
  margin-left: -15px;
  margin-right: -15px;

  &__item {
    margin-bottom: 30px;
  }
}
</style>
