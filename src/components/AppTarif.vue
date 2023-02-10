<template>
  <div class="tarif mt-36">
    <div class="serices__wrapper container mx-auto max-w-6xl">
      <div class="title text-2xl font-bold text-gray text-left mb-16">
        ЗЕЛЕНЫЙ ТАРИФ
      </div>
      <div class="tarif__content flex gap-20 md:flex-row flex-col">
        <div class="tarif__text flex flex-col gap-12 md:w-1/2 w-full">
          <div class="tarif__slider">
            <Swiper
              :slides-per-view="1"
              :space-between="50"
              :modules="[Navigation]"
              :navigation="{
                prevEl: prev,
                nextEl: next,
              }"
            >
              <SwiperSlide>
                <div class="slide flex md:flex-row flex-col gap-10">
                  <img src="/src/assets/slider__img.jpg" alt="" />
                  <div class="slide__text">
                    Цена, по которой домохозяйства могут продать электроэнергию,
                    более чем в 10 раз превышает цену, по которой они ее
                    покупают для своих нужд — 0,16 Евро/кВт (продажа).
                  </div>
                </div>
              </SwiperSlide>
              <SwiperSlide>
                <div class="slide flex md:flex-row flex-col gap-10">
                  <img src="/src/assets/slider__img.jpg" alt="" />
                  <div class="slide__text mb-5">
                    Цена, по которой домохозяйства могут продать электроэнергию,
                    более чем в 10 раз превышает цену, по которой они ее
                    покупают для своих нужд — 0,16 Евро/кВт (продажа).
                  </div>
                </div>
              </SwiperSlide>
              <SwiperSlide>
                <div class="slide flex md:flex-row flex-col gap-10">
                  <img src="/src/assets/slider__img.jpg" alt="" />
                  <div class="slide__text mb-5">
                    Цена, по которой домохозяйства могут продать электроэнергию,
                    более чем в 10 раз превышает цену, по которой они ее
                    покупают для своих нужд — 0,16 Евро/кВт (продажа).
                  </div>
                </div>
              </SwiperSlide>
              <div class="navigation flex gap-6 absolute bottom-0 right-0 z-10">
                <div ref="prev" class="">
                  <IconArrow
                    class="rotate-180 cursor-pointer fill-black hover:fill-accent"
                  />
                </div>
                <div ref="next" class="">
                  <IconArrow
                    class="cursor-pointer fill-black hover:fill-accent"
                  />
                </div>
              </div>
            </Swiper>
          </div>

          <div class="tarif__grid flex flex-wrap gap-y-5">
            <div class="text__block flex flex-col gap-1 md:w-1/2 w-full pr-4">
              <strong>Гарантия выкупа </strong>
              <p>
                Гарантированный выкуп электроэнергии государством - прописано в
                НКРЕ №447
              </p>
            </div>
            <div class="text__block flex flex-col gap-1 md:w-1/2 w-full pr-4">
              <strong>Долгосрочно</strong>
              <p>
                это проект, поддерживаемый международными инвестиционными
                организациями
              </p>
            </div>
            <div class="text__block flex flex-col gap-1 md:w-1/2 w-full pr-4">
              <strong>Вид вложения </strong>
              <p>
                Альтернатива банковским депозитам, окупаемость - от 16% до 18%
                годовых
              </p>
            </div>
            <div class="text__block flex flex-col gap-1 md:w-1/2 w-full pr-4">
              <strong>Высокая ставка</strong>
              <p>Самая высокая тарифная ставка в европе - 0,16 евро</p>
            </div>
          </div>
        </div>
        <div class="tarif__image md:w-1/2 w-full">
          <div class="mb-4">
            <strong>
              «Зеленый тариф» — это особые тарифные условия, которые позволяют
              частным домохозяйствам не только потреблять, но и продавать
              выработанное домашними солнечными электростанциями электричество в
              электросеть общего пользования.
            </strong>
          </div>
          <img src="/src/assets/tarif__img.jpg" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import IconArrow from './UI/Icons/IconArrow.vue';
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Navigation } from 'swiper';
import 'swiper/css';
import 'swiper/css/navigation';
import { ref } from 'vue';

const prev = ref(null);
const next = ref(null);
</script>

<style lang="scss" scoped></style>
