<script setup>
import MyBtn from '../components/MyBtn.vue';
</script>

<template>
  <div class="container">
    <div>
      <h1>Will you go on a date with me?</h1>
      <div class="flex">
        <button class="btn" @click="$router.push('/good-choice')">Yes</button>
        <MyBtn class="btn" style="margin-left: 50px;" />
      </div>
      <img src="https://media.tenor.com/zGm5acSjHCIAAAAC/cat-begging.gif" alt="">
    </div>
  </div>
</template>

<style>
img {
  display: flex;
  justify-content: center;
  margin: 0 auto;
  margin-top: 50px;
}
.container {
  border: 2px solid #FFF8E1;
  padding: 50px;
  border-radius: 30px;
  margin: 0 auto;
  width: 900px;
  display: flex;
  justify-content: center;
}
.flex {
  display: flex;
}
h1{
  color: #FFE5F1;
  margin-bottom: 50px;
}
.btn {
  outline: none;
  border:none;
  cursor: pointer;
  display: block;
  position: relative;
  background-color: #ADA2FF;
  font-size: 16px;
  color: white;
  text-transform: uppercase;
  letter-spacing: 2px;
  padding: 25px 80px;
  border-radius: 20px;
  box-shadow: 0 6px #9f96e2;
  width: fit-content;
}

.btn:hover {
  box-shadow: 0 4px #9f96e2;
  top: 2px;
}

.btn:active {
  box-shadow: none;
  top: 6px;
}
</style>