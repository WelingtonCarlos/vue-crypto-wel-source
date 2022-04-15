<template>
  <div>
    <PriceTop />
    <TableSection />
  </div>
</template>

<script>
import TableSection from "../components/TableSection.vue";
import PriceTop from "../components/PriceTop.vue";

export default {
  name: "Prices",
  components: { TableSection, PriceTop },
};
</script>

<style></style>
