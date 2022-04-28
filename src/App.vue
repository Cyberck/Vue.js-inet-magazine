<template>
    <div id="app">
        <div class="container">
            <nav class="preNav">
                <div class="preNav__sub">
                    <a href="#!" class="preNav__logo">Ткани</a>
                    <div class="preNav__location">
                        <a href="#!" class="preNav__icon">
                  <i class="fa-solid fa-location-dot"></i>
                </a>
                        <div class="preNav__name-location">Санкт-Петербург</div>
                    </div>
                    <form class="preNav__input-parent">
                        <input type="text" class="preNav__input" placeholder="Я ищу" />
                    </form>
                    <div class="preNav__contact-parent">
                        <a href="tel:8 800 900 70 90" class="preNav__tel">8 800 900 70 90</a
                >
                <div class="preNav__time">Пн-вс: 10:00 - 21:00</div>
              </div>
              <div class="preNav__icons-parent">
                <a href="#!" class="preNav__love preIcon">
                  <i class="fa-solid fa-heart"></i>
                </a>
                        <a href="#!" class="preNav__man preIcon">
                  <i class="fa-solid fa-id-badge"></i>
                </a>
                        <a href="#!" class="preNav__bag preIcon">
                  <i class="fa-solid fa-bag-shopping"></i>
                  <span>12</span>
                </a>
                    </div>
                </div>
                <div class="nav__nav">
                    <ul class="nav__list">
                        <li class="nav__link" rel="noopener" v-for="(item, i) in list" :key="i">
                            {{ item }}
                        </li>
                    </ul>
                </div>
            </nav>
        </div>
        <HeaderContent />
        <MainProsentImg />
    </div>
</template>

<script>
import HeaderContent from "./components/HeaderContent.vue";
import MainProsentImg from "./components/MainProsentImg.vue";

export default {
    components: {
        HeaderContent,
        MainProsentImg,
    },
    data() {
        return {
            list: [
                "Для одежды",
                "Для интерьера",
                "Мебельные",
                "Фурнитура",
                "Пряжа",
                "Новогодние",
                "Для шитья",
            ],
        };
    },
};
</script>

<style scoped lang="sass">
*
  margin: 0
  padding: 0
  box-sizing: border-box

ul
  list-style: none

a
  text-decoration: none

.container
  max-width: 1140px
  width: 100%
  margin: 0 auto

.preNav__icon
  font-size: 22px
  color: black

.preNav__logo
  font-family: "Montserrat"
  font-style: normal
  font-weight: 300
  font-size: 48px
  line-height: 150%
  text-transform: uppercase
  color: #bf1e77

nav
  margin-top: 37px

.preNav
  display: flex
  flex-direction: column
  margin-bottom: 17px

  &__sub
    display: flex
    align-items: center
    justify-content: space-between

  &__location
    display: flex
    margin-left: 60px
    margin-right: 40px

  &__icon
    margin-right: 11px

  &__name-location
    font-family: "Montserrat"
    font-style: normal
    font-weight: 400
    font-size: 12px
    line-height: 150%
    color: #545155

  &__input-parent

  &__input
    padding: 12px 16px
    width: 309px
    height: 40px
    background: #fbf7f4
    border-radius: 4px
    flex: none
    order: 1
    flex-grow: 1
    border: none

  &__contact-parent
    margin-left: 50px
    margin-right: 28px

  &__tel
    font-family: "Montserrat"
    font-style: normal
    font-weight: 500
    font-size: 20px
    line-height: 150%
    color: #545155

  &__time
    font-family: "Montserrat"
    font-style: normal
    font-weight: 400
    font-size: 12px
    line-height: 150%
    color: #545155

  &__icons-parent

.preIcon
  padding: 12.8px 16.6px

.preNav__love
  background: #fbf7f4

.preNav__man
  background: #fbf7f4

.preNav__bag
  background: #bf1e77

  & span
    margin-left: 5px

.nav__list
  display: flex
  column-gap: 51px
  justify-content: space-between

.nav__link
  font-family: "Montserrat"
  font-style: normal
  font-weight: 500
  font-size: 16px
  line-height: 150%
  color: #545155
  transition: 0.3s
  cursor: pointer
  display: flex
  flex-direction: column
  align-items: center

  &:hover
    color: #bf1e77

  &::after
    content: ""
    display: block
    height: 1px
    bottom: 0px
    width: 0
    background: #bf1e77
    transition: all ease 300ms

  &:hover.nav__link::after
    width: 100%
</style>
