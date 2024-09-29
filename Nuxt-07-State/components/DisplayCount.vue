<template>
  <div>
    <h3>DisplayCount</h3>
    <p>当前计数: {{ count }}</p>
  </div>
</template>

<script setup>
const count = useState('count', () => 0);  // 共享相同的状态
</script>

<style scoped>
h2 {
  color: #333;
}
</style>