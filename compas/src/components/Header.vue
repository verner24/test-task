<script setup>

</script>

<template>
  <div class="header">
    <div class="container-wrapper header__navbar">
      <div class="header__item">
        <img src="/images/Group.svg" alt="">
        <span>Тарифы</span>
        <span>Контакты</span>
      </div>
      <div class="header__item">
        <a href="tel:+74951184422">+7 495 118-44-22</a>
        <button class="header__btn">Вход</button>
        <button class="btn btn_color_blue">Регистрация</button>
      </div>
    </div>
  </div>
</template>

<style lang="less" scoped>
.header {
  position: sticky;
  top: 0;
  background: linear-gradient(to right, rgba(0, 0, 0, 1), rgba(28, 39, 52, 1));
  width: 100%;
  height: 60px;

  &__navbar {
    display: flex;
    height: 100%;
    justify-content: space-between;
   }
  &__item {
    display: flex;
    align-items: center;
    color: white;
    gap: 30px;
  }
  &__btn {

  }
  &__btn_color_blue {

  }
}
</style>