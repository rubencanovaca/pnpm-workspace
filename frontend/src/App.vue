<script setup lang="ts">
import { AButton, ALink, ALogo } from '@package/bits'
</script>

<template>
  <div class="p-6">
    <ALogo />
    <ALink :link="{ text: 'Google', url: 'https://www.google.com' }" />
    <AButton :link="{ text: 'Google', url: 'https://www.google.com' }" />
  </div>
</template>
