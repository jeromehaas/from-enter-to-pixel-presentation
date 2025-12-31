<script setup>
import { computed, onMounted, onUnmounted, ref } from 'vue';
import Cover from './components/slides/cover.vue';
import JoiningTheNetwork from './components/slides/joining-the-network.vue';
import EnterUrlInBrowser from './components/slides/enter-url-in-browser.vue';
import DnsResolution from './components/slides/dns-resolution.vue';
import ThreeWayHandshake from './components/slides/three-way-handshake.vue';
import TlsHandshake from './components/slides/tls-handshake.vue';
import HopByHopRouting from './components/slides/hop-by-hop-routing.vue';
import Dom from './components/slides/dom.vue';
import Cssom from './components/slides/cssom.vue';
import RenderThree from './components/slides/render-three.vue';
import Paint from './components/slides/paint.vue';
import Connect from './components/slides/connect.vue';

const slideCounter = ref(0);

const slides = [
  Cover,
  JoiningTheNetwork,
  EnterUrlInBrowser,
  DnsResolution,
  ThreeWayHandshake,
  TlsHandshake,
  HopByHopRouting,
  Dom,
  Cssom,
  RenderThree,
  Paint,
  Connect,
];

const currentSlide = computed(() => {
  return slides[slideCounter.value];
});

const currentProgress = computed(() => {
  return 100 / (slides.length - 1) * slideCounter.value;
});

const updateSlide = ({ direction }) => {

  if (direction === 'forward' && slideCounter.value < slides.length - 1) {
    slideCounter.value++;
  }

  if (direction === 'backward' && slideCounter.value > 0) {
    slideCounter.value--;
  }

};

const onKeyboardDown = ({ event }) => {

  const { key } = event;

  if (key === 'ArrowRight') {
    updateSlide({ direction: 'forward' });
  }

  if (key === 'ArrowLeft') {
    updateSlide({ direction: 'backward' });
  }

};

const addEventListeners = () => {
  window.addEventListener('keydown', (event) => onKeyboardDown({ event: event }));
};

const removeEventListeners = () => {
  window.removeEventListener('keydown', onKeyboardDown);
};

onMounted(() => {
  addEventListeners();
});

onUnmounted(() => {
  removeEventListeners();
});
</script>

<template>
  <div class="wrapper">
    <component :is="currentSlide" :slideCounter="slideCounter" :progress="currentProgress"/>
  </div>
</template>
