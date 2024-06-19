<script setup>
import FishForm from "@/FishForm.vue";
import {ref} from "vue";

const show = ref(true);
const selected = ref([]);
const fishName = ref('');

const updateFishSelected = (e) => {
  selected.value.push(e.value);
}

const updateFishName = (e) => {
  console.log("fish name", e)
}

const types = ref(
    [
      {value: 'goldfish', url: '/goldfish.png'},
      {value: 'golden-purple-fish', url: '/golden-purple-fish.png'},
      {value: 'guppie', url: '/guppie.png'},
      {value: 'tropical-fish', url: '/tropical-fish.png'},
      {value: 'tuna', url: '/tuna.png'},
    ]);

</script>
<template>
  <div class="viewport-center aquarium-image">

    <div class="box">
      <img v-for="fish in selected"
           :key="fish"
           class="h-20 center-fish"
           :src="`/${fish}.png`" alt=""
      >
      <span class="font-bold">Fish Bubbles</span>
    </div>

    <FishForm :types="types" @update-fish-type="updateFishSelected" @updateFishName="updateFishName" :fish-name="fishName"/>
  </div>
</template>

<style>
.viewport-center {
  @apply flex items-center justify-center h-screen p-4;
}

.aquarium-image {
  background-image: url("/bg.jpg");
  background-attachment: fixed;
  margin: auto;
  height: 100vh
}

.center-fish {
  @apply flex flex-wrap gap-10 justify-center
}
.box {
  width: 100px;
  height: 100px;
  position: relative;
  animation: myfirst 50s linear 2s infinite alternate;
}

@keyframes myfirst {
  0%   { left:0px; top:0px;}
  50%  { left:400px; top:200px;}
  100%  {left:400px; top:400px;}
}
</style>
