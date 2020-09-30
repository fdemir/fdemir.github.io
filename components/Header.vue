<template>
  <div class="header">
    <div class="header-content container">
      <span class="header-desc"
        >Web <br />
        Development</span
      >
      <div class="header-info">
        <a href="tel:+380932163298" class="header-info__address"
          >+380 93 216 32 98</a
        >
        <a href="mailto:frndemir@gmail.com" class="header-info__address"
          >frndemir@gmail.com</a
        >
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import '~/assets/scss/partials/_breakpoints.scss';

.header {
  width: 100%;
  height: 90px;

  @include bp(tablet) {
    display: none;
  }

  &-nav {
    justify-self: flex-end;

    &__icon {
      width: 30px;
      cursor: pointer;

      > div {
        width: 100%;
        background: #000;
        border-radius: 100px;
        height: 2px;
        &:first-child {
          margin-bottom: 10px;
        }
      }
    }
  }

  &-desc {
    text-transform: uppercase;
    font-weight: 600;
    color: #b0b0b0;
    margin-right: 120px;
    line-height: 23px;
  }

  &-content {
    display: flex;
    align-items: center;
    flex-direction: row;
    height: 100%;
  }

  &-info {
    display: flex;
    flex-direction: row;
    &__address {
      font-weight: 600;
      text-transform: uppercase;
      color: inherit;
      text-decoration: none;
      white-space: nowrap;

      &:not(:last-child):after {
        content: '/';
        margin: 0 10px;
        color: #b0b0b0;
      }
    }
  }
}
</style>
