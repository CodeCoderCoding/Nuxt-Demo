// components/ArticlePreview.vue
<template>
  <div>
    <h2>文章预览</h2>
    <input v-model="article.title" placeholder="输入标题" />
  </div>
</template>

<script setup>
import { useState } from '#app';

const article = useState('article');
</script>