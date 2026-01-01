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
          <img class="content__image" src="/graphics/cover.svg" alt="Cover"/>
        </div>
        <div class="content__right">
          <div class="content__heading">
            <h1 class="content__heading-line">Vom Enter zum Pixel:</h1>
            <h1 class="content__heading-line">der Web-Ladepfad in 6 Schritten</h1>
          </div>
          <div class="content__metadata">
            <p class="content__metadata-line">Klasse: HFIE 2024</p>
            <p class="content__metadata-line">Name der Betreuerin: Pascale Koller</p>
            <p class="content__metadata-line">Name des Verfassers: Jérôme Haas</p>
            <p class="content__metadata-line">Datum der Präsentation: 05.12.2025</p>
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
