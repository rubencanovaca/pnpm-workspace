<script setup lang="ts">
import { defineProps } from 'vue'

import AText from "../atoms/AText.vue"
import ATitle from "../atoms/ATitle.vue"

const props = defineProps({
  card: {
    type: Object,
    default() {
      return {
        title: '',
        text: ''
      }
    }
  }
})
</script>

<template>
  <div
    class="p-6 border border-blue-200 hover:shadow-lg rounded-sm bg-brand-main text-blue-800 transition ease-in-out duration-500"
  >
    <ATitle tag="h2" :content="props.card.title" />
    <AText :text="props.card.text" />
  </div>
</template>