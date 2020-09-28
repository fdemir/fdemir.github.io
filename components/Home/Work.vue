<template>
  <div class="work">
    <div class="work-header">
      <h4 class="work-header__title">{{ data.title }}</h4>
      <h4 class="work-header__subtitle">{{ data.type }}</h4>
    </div>
    <div
      class="work-content"
      :style="`background: url(${require('~/assets/images/' + data.image)})`"
    ></div>
  </div>
</template>

<script>
export default {
  props: {
    data: Object,
  },
}
</script>

<style lang="scss" scoped>
.work {
  width: 100%;
  height: 100%;
  border-radius: 20px;
  background: #f3f4f8;
  position: relative;
  display: flex;
  justify-content: flex-end;
  align-items: flex-end;
  overflow: hidden;

  &-content {
    width: 80%;
    height: 70%;
    border-radius: 20px 0 0 0;
    // @refactor
    background-size: 580px !important;
    background-repeat: no-repeat !important;
    box-shadow: -13px -1px 20px 3px rgba(0, 0, 0, 0.1);
  }

  &-header {
    position: absolute;
    left: 0;
    top: 0;
    padding: 3rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;

    &__title {
      color: #000;
      font-size: 1.5rem;
    }

    &__subtitle {
      color: #a2a2a2;
      font-weight: 400;
    }
  }
}
</style>
