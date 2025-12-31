<script setup>
import './navigation.scss';

defineProps({
  slideCounter: Number,
});
</script>

<template>
  <nav class="navigation">
    <div class="navigation__block" :class="{ 'navigation__block--active': slideCounter >= 1 && slideCounter <= 2 }">
      <p class="navigation__text">Vorbereitung</p>
    </div>
    <div class="navigation__block" :class="{ 'navigation__block--active': slideCounter >= 3 && slideCounter <= 3 }">
      <p class="navigation__text">DNS Auflösung</p>
    </div>
    <div class="navigation__block" :class="{ 'navigation__block--active': slideCounter >= 4 && slideCounter <= 4 }">
      <p class="navigation__text">Verbindungsaufbau</p>
    </div>
    <div class="navigation__block" :class="{ 'navigation__block--active': slideCounter >= 5 && slideCounter <= 5 }">
      <p class="navigation__text">Verschlüsselung</p>
    </div>
    <div class="navigation__block" :class="{ 'navigation__block--active': slideCounter >= 6 && slideCounter <= 6 }">
      <p class="navigation__text">Übermittlung der Dateien</p>
    </div>
    <div class="navigation__block" :class="{ 'navigation__block--active': slideCounter >= 7 && slideCounter <= 10 }">
      <p class="navigation__text">Darstellung im Browser</p>
    </div>
  </nav>
</template>
