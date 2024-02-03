<script>
import MyBtn from '../components/MyBtn.vue';
export default {
  components: {MyBtn},
  data(){
    return {
      isShown: false
    }
  },
  methods: {
    handleClick() {
      this.isShown = true
    }
  }
}
</script>

<template>
  <div class="container">
    <div>
      <div class="flex ar">
        <!-- <router-link to="/" class="arrow">
          <svg xmlns="http://www.w3.org/2000/svg" fill="#9f96e2" width="800px" height="800px" viewBox="0 0 52 52" data-name="Layer 1" id="Layer_1"><path d="M50,24H6.83L27.41,3.41a2,2,0,0,0,0-2.82,2,2,0,0,0-2.82,0l-24,24a1.79,1.79,0,0,0-.25.31A1.19,1.19,0,0,0,.25,25c0,.07-.07.13-.1.2l-.06.2a.84.84,0,0,0,0,.17,2,2,0,0,0,0,.78.84.84,0,0,0,0,.17l.06.2c0,.07.07.13.1.2a1.19,1.19,0,0,0,.09.15,1.79,1.79,0,0,0,.25.31l24,24a2,2,0,1,0,2.82-2.82L6.83,28H50a2,2,0,0,0,0-4Z"/></svg>
        </router-link> -->
        <h1>Good Choice!🩷</h1>
      </div>
      <img src="https://media.tenor.com/aKFaZBrZFYcAAAAM/excited-spin.gif" alt="">
      <!-- <div class="">
        <p>Here is some options:</p>
        <div class="flex">
          <input type="radio" id="1" name="1" value="1">
          <label for="1">Хинкали</label>
        </div>
        <div class="flex">
          <input type="radio" id="4" name="1" value="4">
          <label for="4">Что-то корейское</label>
        </div>
        <div class="flex form-group">
          <input type="checkbox" id="2" name="2" value="2">
          <label for="2">Круассаны</label>
        </div>
        <div class="flex form-group">
          <input type="checkbox" id="3" name="3" value="3">
          <label for="3">Bubble Tea</label>
        </div>
        <div class="you flex">
          <input type="text" placeholder="your opyions">
        </div>
        <button class="btn" @click="handleClick">Submit</button>
      </div>
      <div class="output" v-if="isShown">
        <p>я просто фронтер и не знаю как отправлять форму кудато :(
          <br>
          <span>so take a screenshot please heh♡</span>
        </p>
      </div> -->
    </div>
  </div>
</template>

<style scoped>
.output {
  margin-top: 30px;
  color: #FFF8E1;
}

.ar {
  align-items: center;
  margin-bottom: 50px;
}
.arrow svg{
  width: 24px;
  height: 24px;
}
p {
  margin-bottom: 20px;
}
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
  margin-bottom: 20px;
}
h1{
  color: #FFE5F1;
  margin-bottom: 0;
  margin-left: 20px;
}
.btn {
  outline: none;
  border:none;
  cursor: pointer;
  display: block;
  position: relative;
  background-color: #ADA2FF;
  font-size: 14px;
  color: white;
  text-transform: uppercase;
  letter-spacing: 2px;
  padding: 16px 80px;
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

.form-group input {
  padding: 0;
  height: initial;
  width: initial;
  margin-bottom: 0;
  display: none;
  cursor: pointer;
}

.form-group label {
  position: relative;
  cursor: pointer;
}

.form-group label:before {
  content:'';
  -webkit-appearance: none;
  background-color: transparent;
  border: 2px solid #ADA2FF;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.05), inset 0px -15px 10px -12px rgba(0, 0, 0, 0.05);
  padding: 10px;
  display: inline-block;
  position: relative;
  vertical-align: middle;
  cursor: pointer;
  margin-right: 5px;
}

.form-group input:checked + label:after {
  content: '';
  display: block;
  position: absolute;
  top: 6px;
  left: 9px;
  width: 6px;
  height: 14px;
  border: solid #ADA2FF;
  border-width: 0 2px 2px 0;
  transform: rotate(45deg);
}
[type="radio"]:checked,
[type="radio"]:not(:checked) {
    position: absolute;
    left: -9999px;
}
[type="radio"]:checked + label,
[type="radio"]:not(:checked) + label
{
    position: relative;
    padding-left: 28px;
    cursor: pointer;
    line-height: 20px;
    display: inline-block;
    color: #666;
}
[type="radio"]:checked + label:before,
[type="radio"]:not(:checked) + label:before {
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    width: 24px;
    height: 24px;
    border: 2px solid #ADA2FF;
    border-radius: 100%;
    background: transparent;
}
[type="radio"]:checked + label:after,
[type="radio"]:not(:checked) + label:after {
    content: '';
    width: 10px;
    height: 10px;
    background: #ADA2FF;
    position: absolute;
    top: 7px;
    left: 7px;
    border-radius: 100%;
    -webkit-transition: all 0.2s ease;
    transition: all 0.2s ease;
}
[type="radio"]:not(:checked) + label:after {
    opacity: 0;
    -webkit-transform: scale(0);
    transform: scale(0);
}
[type="radio"]:checked + label:after {
    opacity: 1;
    -webkit-transform: scale(1);
    transform: scale(1);
}
.you input {
  border: 2px solid #FFE5F1;
  background: transparent;
  padding: 3px 10px;
  color: #ADA2FF;
}
</style>

