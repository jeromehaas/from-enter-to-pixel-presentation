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
        <img src="/icons/quote.svg" alt="Zitat"/>
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

.content__metadata {
  margin-top: auto;
  align-self: flex-end;
}
</style>
