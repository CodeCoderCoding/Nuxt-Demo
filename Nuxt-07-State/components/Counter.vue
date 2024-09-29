<template>
  <div>
    <h2>Counter</h2>
    <button @click="increment">增加</button>
    <button @click="decrement">减少</button>
  </div>
</template>

<script setup>
const count = useState('count', () => 0);  // 创建共享状态

function increment() {
  count.value++;  // 增加计数
}

function decrement() {
  if (count.value > 0) {
    count.value--;  // 减少计数
  }
}
</script>

<style scoped>
button {
  margin: 5px;
}
</style>