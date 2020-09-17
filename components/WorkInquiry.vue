<template>
  <div class="work-inquiry">
    <div class="work-inquiry-content container">
      <div class="work-inquiry-box">
        <div>
          <h3 class="work-inquiry-box__title">Work Inquiry</h3>
          <p class="work-inquiry-box__desc">
            Let's work together and i'll help you by all my best.
          </p>
        </div>
        <div>
          <f-button class="btn-secondary">LET'S CHAT</f-button>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.work-inquiry {
  padding-bottom: 10rem;

  &-box {
    margin: 0 auto;
    background: rgba(0, 173, 181, 0.2);
    border-radius: 12px;
    min-height: 250px;
    max-width: 900px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 3rem;

    &__title {
      color: #000;
      font-size: 3rem;
      font-weight: 600;
      margin-bottom: 20px;
    }

    &__desc {
      color: #000;
      font-size: 1rem;
    }
  }
}
</style>
