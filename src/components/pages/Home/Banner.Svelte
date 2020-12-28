<script>
import FButton from '../../ui/FButton.svelte'
</script>

<style lang="scss" scoped>
@import '../../../assets/scss/partials/_breakpoints.scss';

.banner {
  min-height: calc(100vh - 90px);
  width: 100%;
  display: grid;

  @include bp(tablet) {
    height: 100vh;
  }

  &-content {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    align-items: center;
    grid-gap: 20px;
    place-items: center;

    @include bp(tablet) {
      grid-template-columns: 1fr;

      &__img-col {
        order: 1;
      }

      &__text-col {
        order: 2;
      }
    }

    &__title {
      font-size: 4rem;
      margin-bottom: 26px;
    }

    &__subtitle {
      font-size: 1.3rem;
      font-weight: 300;
      margin-bottom: 20px;
    }

    &__desc {
      line-height: 27px;
      color: #a2a2a2;
      margin-bottom: 30px;
    }
  }

  &-img {
    max-width: 100%;
    height: auto;
  }
}
</style>

<div class="banner">
  <div class="banner-content container">
    <div class="banner-content__text-col">
      <h1 class="banner-content__title">Furkan Demir</h1>
      <h2 class="banner-content__subtitle">
        SOFTWARE DEVELOPER AND MUSICIAN
      </h2>
      <p class="banner-content__desc">
        <!-- Lorem ipsum, dolor sit amet consectetur adipisicing elit. Fugit
        ducimus sint cumque eveniet repellendus odit enim fugit ducimus sint
        cumque eveniet.... -->
        Hi. I'm Furkan. I'm passionate about programming, design, music,
        language and filming. I make fast and compatible apps.
      </p>
      <div class="banner-content__btn">
        <a href="#footer">
          <FButton>LET'S CHAT</FButton>
        </a>
      </div>
    </div>
    <div class="banner-content__img-col">
      <img src="/images/banner.webp" class="banner-img" alt="" />
    </div>
  </div>
</div>