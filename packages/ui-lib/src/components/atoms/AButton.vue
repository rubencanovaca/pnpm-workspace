<script setup lang="ts">
import { defineProps } from 'vue'

const props = defineProps({
  link: {
    type: Object,
    default() {
      return {
        url: '',
        text: ''
      }
    }
  }
})
</script>

<template>
  <a
    :href="props.link.url"
    class="block text-center py-1 px-4 bg-brand-main text-blue-500 font-semibold rounded"
  >
    {{ props.link.text }}
  </a>
</template>
