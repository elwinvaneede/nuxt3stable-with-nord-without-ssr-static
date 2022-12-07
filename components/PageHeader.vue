<script lang="ts" setup>
import "@nordhealth/components/lib/Header";

const route = useRoute();
</script>

<template>
  <nord-header slot="header">
    <h1 class="n-typescale-l">{{ route.meta.title }}</h1>
  </nord-header>
</template>
