<script setup lang="ts">
import AButton from "../atoms/AButton.vue"
import AText from "../atoms/AText.vue"
import ATitle from "../atoms/ATitle.vue"
</script>

<template>
  <div class="px-4 pt-40 pb-12 md:py-32 bg-blue-900 text-gray-100">
    <section class="max-w-sm md:max-w-xl mx-auto">
      <ATitle tag="h1" content="Title" />
      <AText
        text="Etiam in arcu lectus. Nulla facilisi. Nunc viverra vehicula nunc eu tristique. Sed gravida libero sem."
      />
      <AButton class="md:max-w-xs" :link="{ text: 'Button', url: '#' }" />
    </section>
  </div>
</template>