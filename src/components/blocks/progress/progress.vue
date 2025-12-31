<script setup>
  import './progress.scss';

  defineProps({
    progress: Number,
  });
</script>

<template>
  <div class="progress">
    <div class="progress__background"></div>
    <div class="progress__status" :style="{ width: `${ progress }%`}"></div>
  </div>
</template>
