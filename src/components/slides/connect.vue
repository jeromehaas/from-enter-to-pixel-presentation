<script setup>
import Slide from '../layouts/slide/slide.vue';
import Progress from '../blocks/progress/progress.vue';
import Content from '../blocks/content/content.vue';

defineProps({
  progress: Number,
  slideCounter: Number
});
</script>

<template>
  <Slide>
    <Progress :progress="progress"/>
    <Content>
      <div class="content">
        <div class="content__left">
          <img class="content__image" src="/qrcodes/website-qrcode.svg" alt="Cover"/>
        </div>
        <div class="content__right">
          <div class="content__heading">
            <h2 class="content__heading-line">Website:</h2>
            <h1 class="content__headint-line">www.ping-pang.ch</h1>
            <br/>
            <h2 class="content__heading-line">Repository:</h2>
            <h1 class="content__headint-line">www.github.com/jeromehaas/from-enter-to-pixel-presentation</h1>
          </div>
        </div>
      </div>
    </Content>
  </Slide>
</template>

<style lang="scss" scoped>
.content {
  display: flex;
  flex-direction: row;
  gap: 24px;
  justify-content: flex-start;
  flex: 1 1 0;
}

.content__left {
  height: 100%;
}

.content__image {
  max-width: 600px;
}

.content__right {
  display: flex;
  flex-direction: column;
  height: 100%;
  padding: 0 48px;
  width: auto;
  flex-grow: 1;
}

.content__heading {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  margin-bottom: 32px;
  width: auto;
}
</style>
