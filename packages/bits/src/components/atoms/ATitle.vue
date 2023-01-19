<script setup lang="ts">
import { defineProps } from 'vue'

const props = defineProps({
  tag: {
    type: String,
    default: ''
  },
  content: {
    type: String,
    default: ''
  }
})
</script>

<template>
  <component :is="props.tag" class="text-gray-50 text-3xl font-serif pb-2">
    {{ props.content }}
  </component>
</template>
