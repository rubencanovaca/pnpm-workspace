<script setup lang="ts">
import { defineProps } from 'vue'

import MLinks from "../molecules/MLinks.vue"

const props = defineProps({
  columnOneLinks: {
    type: Array,
    default() {
      return []
    }
  },
  columnTwoLinks: {
    type: Array,
    default() {
      return []
    }
  }
})
</script>

<template>
  <footer class="flex flex-wrap text-white">
    <div class="w-full md:w-1/4 bg-gray-900 p-4 md:p-12">
      <MLinks class="flex flex-col" :links="props.columnOneLinks" />
    </div>
    <div class="w-full md:w-3/4 bg-blue-900 p-4 md:p-12">
      <MLinks class="flex flex-col" :links="props.columnTwoLinks" />
    </div>
  </footer>
</template>