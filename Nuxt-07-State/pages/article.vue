// pages/index.vue
<template>
  <div>
    <h1>文章管理</h1>
    <TitleEditor />
    <ArticlePreview />
  </div>
</template>

<script setup>
import { useState } from '#app';
import TitleEditor from '~/components/TitleEditor.vue';
import ArticlePreview from '~/components/ArticlePreview.vue';

const articleState = useState('article', () => ({
  id: 0,
  title: '',
  content: '',
}));
</script>