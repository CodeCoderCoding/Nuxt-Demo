<template>
  <div>
    <div v-if="editor">
      <button
          @click="editor.chain().focus().toggleBold().run()"
          :disabled="!editor.can().chain().focus().toggleBold().run()"
          :class="{ 'is-active': editor.isActive('bold') }"
      >
        bold
      </button>
      <button
          @click="editor.chain().focus().toggleItalic().run()"
          :disabled="!editor.can().chain().focus().toggleItalic().run()"
          :class="{ 'is-active': editor.isActive('italic') }"
      >
        italic
      </button>
      <button
          @click="editor.chain().focus().toggleStrike().run()"
          :disabled="!editor.can().chain().focus().toggleStrike().run()"
          :class="{ 'is-active': editor.isActive('strike') }"
      >
        strike
      </button>
      <button
          @click="editor.chain().focus().toggleCode().run()"
          :disabled="!editor.can().chain().focus().toggleCode().run()"
          :class="{ 'is-active': editor.isActive('code') }"
      >
        code
      </button>
      <button @click="editor.chain().focus().unsetAllMarks().run()">
        clear marks
      </button>
      <button @click="editor.chain().focus().clearNodes().run()">
        clear nodes
      </button>
      <button
          @click="editor.chain().focus().setParagraph().run()"
          :class="{ 'is-active': editor.isActive('paragraph') }"
      >
        paragraph
      </button>

      <!-- 下拉列表用于选择标题 -->
      <select @change="setHeading($event.target.value)">
        <option value="">Select Heading</option>
        <option value="1">h1</option>
        <option value="2">h2</option>
        <option value="3">h3</option>
        <option value="4">h4</option>
        <option value="5">h5</option>
        <option value="6">h6</option>
      </select>

      <button
          @click="editor.chain().focus().toggleBulletList().run()"
          :class="{ 'is-active': editor.isActive('bulletList') }"
      >
        bullet list
      </button>
      <button
          @click="editor.chain().focus().toggleOrderedList().run()"
          :class="{ 'is-active': editor.isActive('orderedList') }"
      >
        ordered list
      </button>
      <button
          @click="editor.chain().focus().toggleCodeBlock().run()"
          :class="{ 'is-active': editor.isActive('codeBlock') }"
      >
        code block
      </button>
      <button
          @click="editor.chain().focus().toggleBlockquote().run()"
          :class="{ 'is-active': editor.isActive('blockquote') }"
      >
        blockquote
      </button>
      <button @click="editor.chain().focus().setHorizontalRule().run()">
        horizontal rule
      </button>
      <button @click="editor.chain().focus().setHardBreak().run()">
        hard break
      </button>
      <button
          @click="editor.chain().focus().undo().run()"
          :disabled="!editor.can().chain().focus().undo().run()"
      >
        undo
      </button>
      <button
          @click="editor.chain().focus().redo().run()"
          :disabled="!editor.can().chain().focus().redo().run()"
      >
        redo
      </button>
    </div>
    <TiptapEditorContent :editor="editor" />
  </div>
</template>

<script setup>
const editor = useEditor({
  content: "<p>I'm running Tiptap with Vue.js. 🎉</p>",
  extensions: [TiptapStarterKit],
});

onBeforeUnmount(() => {
  unref(editor).destroy();
});
</script>
