<script setup>
import hero from "@/components/hero.vue";
import homecard from "@/components/homecard.vue";
import joblisting from "@/components/joblisting.vue";
</script>

<template>
  <hero />
  <homecard />
  <joblisting :limit="3" :showButton="true" />
</template>

<style scoped></style>
