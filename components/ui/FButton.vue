<template>
  <button class="btn" :class="customClass"><slot /></button>
</template>

<script>
export default {
  props: {
    customClass: { type: String, default: '' },
  },
}
</script>

<style lang="scss" scoped>
.btn {
  padding: 0.8rem 1.25rem;
  background: #222831;
  outline: none;
  border: 0;
  cursor: pointer;
  border-radius: 10px;
  color: #fff;
  font-weight: 500;
  font-size: 1rem;
  transition: transform 0.1s ease-in;

  &-secondary {
    background: #393e46;
  }

  &:active {
    transform: scale(0.9);
  }
}
</style>
