<template>
  <div class="works-section">
    <div class="container">
      <div class="works-section-header">
        <div>
          <h3 class="works-section-header__title">Works</h3>
          <h5 class="works-section-header__subtitle">
            Featured projects, lorem ipsum dolor sit amet...
          </h5>
        </div>
        <div>deneme</div>
      </div>
      <div>
        <flickity ref="flickity" :options="flickityOptions">
          <div class="carousel-cell" v-for="x in 4" :key="x">
            <Work />
          </div>
        </flickity>
      </div>
    </div>
  </div>
</template>

<script>
import Flickity from 'vue-flickity'
export default {
  components: {
    Flickity,
  },
  data() {
    return {
      flickityOptions: {
        groupCells: 1,
        cellAlign: 'left',
        pageDots: false,
        prevNextButtons: false,
      },
    }
  },
}
</script>

<style lang="scss" scoped>
.works-section {
  padding-bottom: 10rem;

  .carousel-cell {
    width: 50%;
    height: 450px;
    margin-right: 20px;
  }

  &-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-bottom: 50px;

    &__title {
      color: #000;
      font-size: 4rem;
      margin-bottom: 20px;
    }

    &__subtitle {
      color: #a2a2a2;
      font-size: 1rem;
      font-weight: 400;
    }
  }
}
</style>
