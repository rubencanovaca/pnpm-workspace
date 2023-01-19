<script setup lang="ts">
import { defineProps } from 'vue'

const props = defineProps({
  text: {
    type: String,
    default: ''
  },
})
</script>

<template>
  <p class="text-gray-300 pb-6">{{ props.text }}</p>
</template>
