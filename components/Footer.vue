<template>
  <div class="footer">
    <a name="footer"></a>
    <div class="footer-content">
      <h4 class="stay-connected">Stay Connected</h4>
      <div class="footer-content__info">
        <span class="location">Kharkiv, Ukraine</span>
        <a href="mailto:info@furkandemir.dev">info@furkandemir.dev</a>
        <a href="tel">+380 93 216 32 98</a>
      </div>
    </div>
    <div class="footer-bottom">
      <div class="footer-bottom__item"></div>
      <div class="footer-bottom__item">
        <ul class="footer-nav">
          <li class="footer-nav__item">
            <n-link to="/">ABOUT</n-link>
          </li>
          <li class="footer-nav__item">
            <n-link to="/">WORKS</n-link>
          </li>
          <li class="footer-nav__item">
            <n-link to="/">SERVICES</n-link>
          </li>
          <li class="footer-nav__item">
            <n-link to="/">NEWS</n-link>
          </li>
          <li class="footer-nav__item">
            <n-link to="/">CONTACT</n-link>
          </li>
        </ul>
      </div>
      <div class="footer-bottom__item">2020 ALL RIGHTS RESERVED</div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import '~/assets/scss/partials/breakpoints';

.footer {
  display: flex;
  flex-direction: column;

  @include bp(tablet-sm) {
    &-bottom {
      height: auto !important;
      grid-template-columns: 1fr !important;

      &__item {
        padding-bottom: 1rem;
        justify-content: center !important;
      }
    }

    &-nav {
      flex-direction: column;
    }
  }

  &::after {
    content: '';
    display: block;
    width: 100%;
    height: 10px;
    background: #00adb5;
  }

  &-content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding-bottom: 35px;

    .stay-connected {
      font-weight: 600;
      font-size: 1.8rem;
      margin-bottom: 30px;
    }

    &__info {
      display: flex;
      flex-direction: column;
      align-items: center;

      .location {
        color: #a5a5a5;
        font-size: 1.1rem;
        margin-bottom: 15px;
      }

      a {
        text-decoration: none;
        color: inherit;
        &[href^='mailto'] {
          margin-bottom: 15px;
          font-size: 2rem;
        }
      }
    }
  }

  &-bottom {
    height: 100px;
    width: 100%;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    padding: 0 3rem;

    &__item {
      display: flex;
      align-items: center;
      justify-content: center;

      &:first-child {
        justify-content: flex-start;
      }

      &:last-child {
        justify-content: flex-end;
        white-space: nowrap;
        text-transform: uppercase;
        font-weight: 300;
      }
    }
  }

  &-nav {
    gap: 20px;
    list-style: none;
    display: flex;
    justify-content: center;
    align-items: center;

    li a {
      color: inherit;
      text-decoration: none;
    }
  }
}
</style>
