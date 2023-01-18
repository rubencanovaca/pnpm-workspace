<script setup lang="ts">
import { defineProps } from 'vue'

import MCard from "../molecules/MCard.vue"

const props = defineProps({
  cards: {
    type: Array,
    default() {
      return []
    }
  }
})
</script>

<template>
  <div class="flex flex-wrap items-stretch md:-mr-4">
    <div v-for="card in props.cards" :key="card.name" class="w-full md:w-1/3 md:pr-4 pb-4">
      <MCard class="h-full" :card="card" />
    </div>
  </div>
</template>