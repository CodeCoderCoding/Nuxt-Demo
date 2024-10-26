// components/TitleEditor.vue
<template>
  <div>
    <h2>编辑标题</h2>
    <input v-model="article.title" placeholder="输入标题" />
  </div>
</template>

<script setup>
import { useState } from '#app';

const article = useState('article');

// 这里不需要额外的代码，v-model 会自动更新状态
</script>