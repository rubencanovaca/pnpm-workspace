<script setup lang="ts">
import { defineProps } from 'vue'

import AButton from "../atoms/AButton.vue"
import ALogo from "../atoms/ALogo.vue"
import MLinks from "../molecules/MLinks.vue"

const props = defineProps({
  links: {
    type: Array,
    default() {
      return []
    }
  }
})
</script>

<template>
  <header class="absolute inset-x-0 text-gray-100 py-4 flex flex-wrap items-center">
    <div class="w-full md:w-3/4 px-4 pb-4 md:pb-0 flex items-center justify-between">
      <ALogo />
      <MLinks class="flex" :links="props.links" />
    </div>
    <div class="w-full md:w-1/4 px-4">
      <AButton :link="{ text: 'Button', url: '#' }" />
    </div>
  </header>
</template>