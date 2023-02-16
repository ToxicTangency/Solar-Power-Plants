<template>
  <footer class="footer pt-16 pb-12" id="form">
    <div class="footer__wrapper container mx-auto max-w-6xl flex flex-col">
      <div class="footer__top flex md:flex-row flex-col md:gap-0 gap-6">
        <div class="footer__form md:w-1/2 w-full md:pr-20">
          <div class="text-white text-2xl uppercase font-bold mb-14">
            ОСТАВИТЬ ЗАЯВКУ
          </div>
          <form class="flex flex-col gap-16" method="POST" data-netlify="true">
            <input
              class="bg-transparent text-white border-b-2 pb-2 focus:outline-0"
              type="text"
              placeholder="Имя"
              v-model="name"
            />
            <input
              class="bg-transparent text-white border-b-2 pb-2 focus:outline-0"
              type="tel"
              placeholder="Телефон"
              v-model="phone"
              v-maska
              data-maska="+7 (###) ##-##-##"
            />
            <AppEnroll
              @click="sumbitForm"
              class="mt-16 ml-10 text-white"
              :variant="'white'"
            />
            <button type="submit">Test</button>
          </form>
        </div>
        <div class="footer__contacts md:w-1/2 w-full">
          <div class="text-white text-2xl uppercase font-bold mb-14">
            КОНТАКТЫ
          </div>
          <div class="footer__contacts-text flex flex-col gap-7">
            <p class="text-white">
              Центральный офис: г. Москва, ул,Гоголя 13, 1й этаж
            </p>
            <p class="text-white">
              +7 000 000-00-00<br />
              +38 000 000-00-00
            </p>
            <p class="text-white">Ежедневно 08:00 - 20:00</p>
          </div>
        </div>
      </div>
      <div
        class="footer__bottom flex md:flex-row flex-col justify-between mt-36 items-center md:gap-0 gap-4"
      >
        <div class="terms text-white">
          <a href="#">Политика конфиденциальности</a>
        </div>
        <div class="logo">
          <IconLogo />
        </div>
        <div class="iconsRow flex gap-5 items-center">
          <a href="mailto:test@gmail.com"
            ><IconMail class="fill-white scale-75"
          /></a>
          <a href="tel:+70000000000"
            ><IconPhone class="fill-white scale-75"
          /></a>
          <a href="https://t.me/"><IconTelegram class="fill-white" /></a>
        </div>
      </div>
    </div>
    <Transition>
      <div
        @click.self="(isModal = false), clearForm()"
        class="modal fixed w-full h-full bottom-0 z-20"
        v-show="isModal"
      >
        <div
          class="modal__box top-1/2 left-1/2 p-6 bg-gray flex justify-between"
        >
          <div class="modal__text text-white">
            {{ name }}, ваша заявка отправлена!<br />
            Наш менеджер свяжется с вами по телефону который Вы указали!
          </div>
          <div
            class="modal__close text-white text-3xl cursor-pointer hover:text-accent"
            @click="(isModal = false), clearForm()"
          >
            x
          </div>
        </div>
      </div>
    </Transition>
  </footer>
</template>

<script setup>
import { ref } from 'vue';
import AppEnroll from './UI/AppEnroll.vue';
import IconLogo from './UI/Icons/IconLogo.vue';
import IconMail from './UI/Icons/IconMail.vue';
import IconPhone from './UI/Icons/IconPhone.vue';
import IconTelegram from './UI/Icons/IconTelegram.vue';
import { vMaska } from 'maska';

const name = ref('');
const phone = ref('');
const isModal = ref(false);

const validate = () => {
  if (name.value === '' || phone.value.length < 17) {
    return false;
  } else {
    return true;
  }
};

const clearForm = () => {
  name.value = '';
  phone.value = '';
};

const sumbitForm = () => {
  if (validate()) {
    isModal.value = true;
  } else {
    alert('Заполните все поля!');
  }
};
</script>

<style scoped>
.footer {
  background-image: url('/src/assets/footer__bg.png');
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed;
}
</style>
