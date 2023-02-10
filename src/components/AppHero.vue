<script setup>
import AppEnroll from './UI/AppEnroll.vue';
import IconLogo from './UI/Icons/IconLogo.vue';
import IconMail from './UI/Icons/IconMail.vue';
import IconPhone from './UI/Icons/IconPhone.vue';
import IconTelegram from './UI/Icons/IconTelegram.vue';
</script>

<template>
  <div class="hero flex flex-col min-h-screen">
    <div class="logo mx-auto mt-16">
      <IconLogo />
    </div>
    <div class="subTitle mx-auto mt-36 text-lg text-white">
      Зеленый тариф для дома и бизнеса
    </div>
    <div class="title mx-auto md:text-6xl text-2xl text-white">
      Солнечная электростанция
    </div>
    <div class="addTitle mx-auto text-white md:text-5xl text-xl">
      с доходом от 1000 $ в месяц
    </div>
    <a href="#form" class="mx-auto mt-28">
      <AppEnroll class="text-white" :variant="'white'" />
    </a>
    <div class="iconsRow mx-auto mt-auto mb-9 flex gap-5 items-center">
      <a href="mailto:test@gmail.com"
        ><IconMail class="fill-white scale-75"
      /></a>
      <a href="tel:+70000000000"><IconPhone class="fill-white scale-75" /></a>
      <a href="https://t.me/"><IconTelegram class="fill-white" /></a>
    </div>
  </div>
</template>

<style scoped>
.hero {
  background-image: url('/src/assets/hero__bg.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed;
}
</style>
