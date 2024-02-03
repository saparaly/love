<template>
    <div id="emcee" :style="boxStyle" @mouseenter="moveButton" @click="showAlert">
      no
    </div>
</template>
  
<script>
  export default {
    data() {
      return {
        boxStyle: {
          left: '0',
          top: '0'
        }
      };
    },
    methods: {
      moveButton() {
        const randX = Math.floor(Math.random() * (window.innerWidth - 1100));
        const randY = Math.floor(Math.random() * (window.innerHeight - 500)); // Adjusted to keep the button within the viewport
        this.boxStyle.left = randX + 'px';
        this.boxStyle.top = randY + 'px';
      },
      showAlert() {
        alert('clicked!');
      }
    }
  };
</script>
  
<style>
</style>
  