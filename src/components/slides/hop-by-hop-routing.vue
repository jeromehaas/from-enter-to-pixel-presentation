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
    <Header>Hop-by-Hop Routing</Header>
    <Content>
      <div class="content">
        <img class="content__image" src="/graphics/hop-by-hop-routing.svg" alt="Hop-by-Hop-Routing"/>
      </div>
    </Content>
    <Navigation :slideCounter="slideCounter"/>
  </Slide>
</template>

<style lang="scss" scoped>
.content {

  .content__image {
    max-width: 800px;
  }

}
</style>
