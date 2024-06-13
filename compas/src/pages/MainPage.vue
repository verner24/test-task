<script setup>
import Header from '../components/Header.vue'

const advantages = [
  {
    id: 1,
    imageUrl: '/images/Infinity.svg',
    title: 'Неограниченый автопарк',
    subtitle: 'Можно добавить неограниченное кол-во машин и водителей'
  },
  {
    id: 2,
    imageUrl: '/images/Ring.svg',
    title: 'Уведомление о погашении',
    subtitle: 'Мы оповестим вас о том, что штраф был погашен и соответствующая запись создана в ГИС ГМП'
  },
  {
    id: 3,
    imageUrl: '/images/Map.svg',
    title: 'Сокращение затрат до 50%',
    subtitle: 'Максимально быстро узнаете о штрафах в автоматическом режиме, тем самым у вас есть время оплатить по скидке'
  },
  {
    id: 4,
    imageUrl: '/images/List.svg',
    title: 'Квитанция об оплате',
    subtitle: 'После совершения оплаты банковской картой на Вашу электронную почту придет квитанция об успешной оплате.'
  },
  {
    id: 5,
    imageUrl: '/images/Secure.svg',
    title: 'Безопасность',
    subtitle: 'Данные передаются в зашифрованном виде, они доступны только получателю'
  },
  {
    id: 6,
    imageUrl: '/images/Time.svg',
    title: 'Все история сохраняется по каждой машине',
    subtitle: 'Вся история штрафов сохраняется по машине и водителю, позволяет анализировать статистику по штрафам'
  }
]
</script>

<template>
  <Header />
  <section class="container-wrapper form">
    <form>
      <div class="form__flex form__flex_column">
        <div class="title-1">
          Проверьте штрафы и зарегестрируйтесь в 1 клик
        </div>
        <div class="form__flex">
          <div class="form__item form__item_grow_m">
            <label>Номер автомобиля</label>
            <input type="text" class="form__input">
          </div>
          <div class="form__item form__item_grow_s">
            <label>Регион</label>
            <input type="text" class="form__input">
          </div>
        </div>
        <div class="form__item">
          <label>Свидетельство о регистрации ТС</label>
          <input type="text" class="form__input">
        </div>
      </div>
      <div class="form__flex ma-1">
        <button class="btn btn_color_blue">
          Проверить штрафы
          <img src="/images/Path.svg" alt="">
        </button>
        <button class="form__btn form__btn_border_blue">
          <img src="/images/Youtube.svg" alt="">
          О сервисе
          <span class="text-blue">(1 мин. 20 сек)</span>
        </button>
      </div>
      <span class="grey-text">
        Нажимая «Проверить штрафы» вы соглашаетесь с политикой обработки персональных данных и принимаете оферту
      </span>
    </form>
    <img src="/images/device.png" alt="">
  </section>
  <section class="container-wrapper advantages">
    <div class="advantages__title title-2">
      Плюсы использования сервиса «Компас» для анализа штрафов
    </div>
    <div v-for="advantage in advantages">
      <div class="advantages__item">
        <img :src="advantage.imageUrl" alt="">
        <div>
          <span class="subtitle">
            {{ advantage.title }}
          </span><br />
          <span class="text">
            {{ advantage.subtitle }}
          </span>
        </div>
      </div>
    </div>
  </section>
  <section class="documents">
    <div class="title-2">
      Документы
    </div>
  </section>
</template>

<style lang="less" scoped>
.swiper {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
}

@media (max-width: 760px) {
  .swiper-button-next {
    right: 20px;
    transform: rotate(90deg);
  }

  .swiper-button-prev {
    left: 20px;
    transform: rotate(90deg);
  }
}
.form {
  display: flex;
  padding-top: 80px;

  &__item {
    display: flex;
    flex-direction: column;
    margin: 30px 30px 0 0;
  }
  &__item_grow_s {
    flex-grow: 1;
  }
  &__item_grow_m {
    flex-grow: 2;
  }
  &__input {
    border: 1px solid #BCBCBC;
    border-radius: 8px;
    height: 40px;
  }
  &__flex_column {
    display: flex;
    flex-direction: column;
  }
  &__flex {
    display: flex;
  }
  &__btn_border_blue {
    border: 1px solid #0584FE;
    color: black;
    padding: 9px 18px;
    box-sizing: border-box;
    margin-left: 21px;
  }
}
.advantages {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-column-gap: 35px;
  grid-row-gap: 35px;

  &__title {
    margin-top: 100px;
    grid-column-start: 1;
    grid-column-end: 4;
    grid-row-start: 1;
    grid-row-end: 3;
  }
  &__item {
    width: 362px;
    height: 174px;
    align-content: center;
    background-color: #FBFCFD;
    border: 1px solid #EEEFF1;
    border-radius: 10px;
    padding: 20px 20px;
    display: grid;
    grid-template-columns: 1fr 4fr;
  }
}
</style>