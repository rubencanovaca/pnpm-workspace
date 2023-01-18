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
  <a :href="props.link.url">{{ props.link.text }}</a>
</template>
