<template>
  <div class="relative enrollBtn group cursor-pointer">
    <IconBtn
      class="absolute -top-14 -left-10 group-hover:bg-accent rounded-full"
      :variant="props.variant"
    />
    <div class="enrollText text-lg z-10 relative">
      записаться на консультацию
    </div>
  </div>
</template>

<script setup>
import IconBtn from './Icons/IconBtn.vue';

const props = defineProps({
  variant: String,
});
</script>

<style lang="scss" scoped></style>
