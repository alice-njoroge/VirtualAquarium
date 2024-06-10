<script setup></script>
<template>
  <div class="fish-form-wrapper bg-blue-700 h-100vh p-2">
    <div>
      <h2 class="text-white font-bold m-2"> Fish Type </h2>
    </div>
    <div class="h-80 m-5 flex flex-wrap justify-between">
      <img class="h-20" src="/goldfish.png" alt="gold">
      <img class="h-20" src="/golden-purple-fish.png" alt="gold">
      <img class="h-20" src="/guppie.png" alt="gold">
      <img class="h-20" src="/tropical-fish.png" alt="gold">
      <img class="h-20" src="/tuna.png" alt="gold">
    </div>
    <div class="mb-4">
      <label class="block text-white font-bold mb-2" for="username">
        Name
      </label>
      <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="username" type="text" placeholder="Mr.Buttons">
    </div>
    <div>
      <button class="bg-red-700 hover:bg-red-800 text-white w-full font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline" type="button">
        Add Fish
      </button>
    </div>
  </div>
</template>
<style scoped>
.fish-form-wrapper{
  position: absolute;
  width: 300px;
  top: 0;
  left: 0;
  z-index: 1;
  border: 1px solid black;
  height: 100%;
}
</style>
