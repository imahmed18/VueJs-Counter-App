<template>
  <div class="counter">
    <h2 class="heading-main">Counter: {{ count }}</h2>
    <div class="btn-wrapper">
      <button class="btn decrement" @click="decrement">-</button>
      <button class="btn increment" @click="increment">+</button>
    </div>
    <button class="btn reset" @click="reset">Reset</button>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  setup() {
    const count = ref(0);
    function increment() {
      count.value++;
      console.log(count);
    }
    function decrement() {
      count.value--;
      console.log(count);
    }
    function reset() {
      count.value = 0;
      console.log(count);
    }
    return {
      count,
      increment,
      decrement,
      reset,
    };
  },
};
</script>

<style scoped>
.counter {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  max-width: 100vw;
  margin: 0 auto;
  height: calc(100vh - 60px);
  flex-direction: column;
  animation: fadeIn 1s ease-in-out;
}
.heading-main {
  font-size: 5.2rem;
  margin-bottom: 16px;
  text-align: center;
  font-weight: bolder;
}
.btn-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
  margin: 10px;
}
.btn {
  width: 100px;
  height: 50px;
  font-weight: 600;
  font-size: 18px;
  outline: none;
  border: none;
  border-radius: 10px;
  color: black;
  box-shadow: 3px 3px 6px #555;
}
.btn.reset {
  background-color: rgb(255, 8, 8);
}

.btn.increment {
  background-color: #42b883;
}

.btn.decrement {
  background-color: #42b883;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
