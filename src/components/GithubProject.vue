<template>
  <div class="dynamic-text-container">
    <span v-html="text"></span>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const text = ref('');

const texts = [
  '二零二一年八月',
  '我...',
  '.',
  '.',
  '.',
  '，',
  '我',
  '想',
  '要',
  '告',
  '诉',
  '你',
  '，',
  '我',
  '很',
  '想',
  '你',
];

let index = 0;

setInterval(() => {
  if (index < texts.length) {
    text.value += texts[index];
    index++;
  }
}, 100);
</script>

<style scoped>
.dynamic-text-container {
  font-size: 24px;
  font-weight: bold;
  color: #fff;
  text-align: center;
}

.dynamic-text-container span {
  display: inline-block;
}
</style>
