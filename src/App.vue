<script setup>

import FishForm from "@/FishForm.vue";
</script>
<template>
  <div class="view-port center aquarium-image">
    <FishForm/>
  </div>
</template>

<style>
.aquarium-image {
  background-image: url("/bg.jpg");
  background-attachment: fixed;
  margin: auto;
  height: 100vh
}
</style>
