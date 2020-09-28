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
        <div>
          <f-button
            class="btn-outline-secondary action-btn"
            @click.native="prev"
            ><ChevronBack
          /></f-button>
          <f-button
            class="btn-outline-secondary action-btn"
            @click.native="next"
            ><ChevronForward
          /></f-button>
        </div>
      </div>
      <div>
        <flickity ref="flickity" :options="flickityOptions">
          <div
            class="carousel-cell"
            v-for="(item, index) in works"
            :key="index"
          >
            <Work :data="item" />
          </div>
        </flickity>
      </div>
    </div>
  </div>
</template>

<script>
import Flickity from 'vue-flickity'
import ChevronBack from 'ionicons/dist/svg/chevron-back-sharp.svg?inline'
import ChevronForward from 'ionicons/dist/svg/chevron-forward-sharp.svg?inline'

const works = [
  {
    title: 'Otokirala',
    type: 'Web Application',
    image: 'otokirala.png',
  },
  {
    title: 'Kamerdam',
    type: 'Web Application',
    image: 'kamerdam.jpg',
  },
  {
    title: 'Preminyum',
    type: 'Web Site',
    image: 'preminyum.png',
  },
  {
    title: 'Uxdev',
    type: 'Web Application',
    image: 'uxdev.png',
  },
]

export default {
  components: {
    ChevronBack,
    Flickity,
    ChevronForward,
  },
  data() {
    return {
      flickityOptions: {
        groupCells: 1,
        cellAlign: 'left',
        pageDots: false,
        prevNextButtons: false,
      },
      works,
    }
  },
  methods: {
    prev() {
      this.$refs.flickity.previous()
    },
    next() {
      this.$refs.flickity.next()
    },
  },
}
</script>

<style lang="scss" scoped>
.works-section {
  padding-bottom: 10rem;

  .action-btn {
    padding: 0;
    width: 45px;
    height: 45px;
    display: inline-grid;
    place-items: center;
  }

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
