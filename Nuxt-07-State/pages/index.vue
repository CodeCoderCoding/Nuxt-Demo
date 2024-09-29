<template>
  <div>
    <Counter />
    <hr/>
    <DisplayCount />
  </div>
</template>

<script setup>
import Counter from '~/components/Counter.vue';
import DisplayCount from '~/components/DisplayCount.vue';
</script>

<style scoped>
div {
  text-align: center;
}
</style>