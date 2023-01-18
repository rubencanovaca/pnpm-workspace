<script lang="ts">
import MBanner from "../components/molecules/MBanner.vue"
import OFooter from "../components/organisms/OFooter.vue"
import OGrid from "../components/organisms/OGrid.vue"
import OHeader from "../components/organisms/OHeader.vue"

export default {
  name: 'TDashboard',
  components: {
    MBanner,
    OFooter,
    OGrid,
    OHeader
  },
  data() {
    return {
      links: [{ text: "Header link 1", url: "#" }],
      cards: [
        {
          title: "Card 1",
          text: "Sed gravida libero sem, sed ornare arcu venenatis at."
        },
        {
          title: "Card 2",
          text: "Etiam in arcu lectus. Nulla facilisi. Nunc viverra vehicula nunc eu tristique."
        },
        {
          title: "Card 3",
          text: "Sed gravida libero sem, etiam in arcu lectus."
        }
      ],
      columnOneLinks: [
        { text: "Footer column 1", url: "#" },
        { text: "Footer column 1", url: "#" }
      ],
      columnTwoLinks: [
        { text: "Footer column 2", url: "#" },
        { text: "Footer column 2", url: "#" }
      ]
    }
  }
}
</script>

<template>
  <main class="flex flex-col min-h-screen">
    <OHeader :links="links" />
    <div class="flex-auto flex flex-wrap bg-white">
      <MBanner class="w-full md:w-3/4 text-center md:text-left" />
      <div class="container mx-auto px-4 py-8 md:py-16">
        <OGrid :cards="cards" />
      </div>
    </div>
    <OFooter :column-one-links="columnOneLinks" :column-two-links="columnTwoLinks" />
  </main>
</template>