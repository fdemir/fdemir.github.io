<template>
  <div class="social-media">
    <div>
      <a href="" class="social-media__link">x</a>
    </div>
    <div>
      <a href="" class="social-media__link">y</a>
    </div>
    <div>
      <a href="" class="social-media__link">z</a>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.social-media {
  position: fixed;
  left: 0;
  top: 0;
  height: 100vh;
  width: 60px;
  background: transparent;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  grid-gap: 30px;

  &__link {
    text-decoration: none;
    font-size: 24px;
  }
}
</style>
