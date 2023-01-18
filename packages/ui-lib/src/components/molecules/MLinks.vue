<script setup lang="ts">
import { defineProps } from 'vue'

import ALink from "../atoms/ALink.vue"

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
  <ul>
    <li v-for="(link, index) in props.links" :key="index">
      <ALink :link="link"/>
    </li>
  </ul>
</template>