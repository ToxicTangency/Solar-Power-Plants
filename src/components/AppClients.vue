<template>
  <div class="clients mt-36">
    <div class="serices__wrapper container mx-auto max-w-6xl">
      <div class="title text-2xl font-bold text-gray text-left mb-16">
        НАШИ КЛИЕНТЫ
      </div>
      <div class="clients__content flex gap-20">
        <div class="clients__text flex flex-col gap-12 w-full">
          <div class="clients__slider">
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
                  <img src="/src/assets/client__img.jpg" alt="" />
                  <div class="slide__text">
                    <div class="flex flex-col gap-8">
                      <strong>
                        Солнечная электростанция 30 кВт подключенная по Зеленому
                        Тарифу
                      </strong>
                      <p class="ml-12">
                        Чистый доход за вычетом налогов с мая 2018 г. по май
                        2019 г. 11 200 $.<br />
                        Смонтирована: апрель 2018 г.<br />
                        Срок службы: 25-30 лет
                      </p>
                    </div>
                    <div class="mt-32 ml-10">
                      <a href="#form"
                        ><AppEnroll class="text-black" :variant="'black'"
                      /></a>
                    </div>
                  </div>
                </div>
              </SwiperSlide>
              <SwiperSlide>
                <div class="slide flex md:flex-row flex-col gap-10">
                  <img src="/src/assets/client__img.jpg" alt="" />
                  <div class="slide__text">
                    <div class="flex flex-col gap-8">
                      <strong>
                        Солнечная электростанция 30 кВт подключенная по Зеленому
                        Тарифу
                      </strong>
                      <p class="ml-12">
                        Чистый доход за вычетом налогов с мая 2017 г. по май
                        2019 г. 13 900 $.<br />
                        Смонтирована: апрель 2017 г.<br />
                        Срок службы: 25-30 лет
                      </p>
                    </div>

                    <div class="mt-32 ml-10">
                      <a href="#form"
                        ><AppEnroll class="text-black" :variant="'black'"
                      /></a>
                    </div>
                  </div>
                </div>
              </SwiperSlide>
              <div class="navigation flex mt-8 gap-6 justify-center">
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
import AppEnroll from './UI/AppEnroll.vue';

const prev = ref(null);
const next = ref(null);
</script>

<style lang="scss" scoped></style>
