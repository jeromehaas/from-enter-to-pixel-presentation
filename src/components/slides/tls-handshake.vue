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
    <Header>TLS-Handshake</Header>
    <Content>
      <div class="content">
        <img class="content__image" src="/graphics/tls-handshake.svg" alt="TLS-Handshake"/>
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
