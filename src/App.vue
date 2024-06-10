<script setup>
import FishForm from "@/FishForm.vue";
import {ref} from "vue";

const show = ref();

</script>
<template>
  <div class="viewport-center aquarium-image">
    <div class="center-fish">
      <img class="h-20" src="/golden-purple-fish.png" alt="" :style="{display: 'block'}">
    </div>
    <FishForm/>
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

.box {
  margin: 30px;
  height: 50px;
  width: 100px;
  background-color: blue;
}

.box.horizTranslate {
  -webkit-transition: 10s;
  -moz-transition: 10s;
  -ms-transition: 10s;
  -o-transition: 10s;
  transition: 10s;
  margin-left: 50% !important;
}

.center-fish {
  @apply flex flex-wrap gap-10 justify-center
}
</style>
