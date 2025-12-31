<script setup>
import Slide from '../layouts/slide/slide.vue';
import Progress from '../blocks/progress/progress.vue';
import Header from '../blocks/header/header.vue';
import Content from '../blocks/content/content.vue';
import Navigation from '../blocks/navigation/navigation.vue';

defineProps({
  progress: Number,
  slideCounter: Number
});
</script>

<template>
  <Slide>
    <Progress :progress="progress"/>
    <Header>CSSDOM</Header>
    <Content>
      <div class="content">
        <img src="/graphics/cssom.svg" alt="CSSOM"/>
      </div>
    </Content>
    <Navigation :slideCounter="slideCounter"/>
  </Slide>
</template>

<style lang="scss" scoped>
.content {

  .content__image {
    max-width: 600px;
  }

}
</style>
