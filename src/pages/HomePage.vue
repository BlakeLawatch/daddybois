<template>
  <template>
    <div class="component">


    </div>
  </template>


  <script>
 import { AppState } from '../AppState';
 import { computed, reactive, onMounted } from 'vue';
 export default {
  setup(){
  return {  }
  }
 };
 </script>


  <style lang="scss" scoped>

  </style>
</template>


<style scoped lang="scss">
.home {
  display: grid;
  height: 80vh;
  place-content: center;
  text-align: center;
  user-select: none;

  .home-card {
    width: clamp(500px, 50vw, 100%);

    >img {
      height: 200px;
      max-width: 200px;
      width: 100%;
      object-fit: contain;
      object-position: center;
    }
  }
}
</style>
