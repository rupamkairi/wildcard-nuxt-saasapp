<template>
  <div>
    <NuxtWelcome />

    <code>{{ subdomain }}</code>
  </div>
</template>

<script setup>
const ssr = useNuxtApp()?.ssrContext;
const host = ssr?.event?.node?.req?.headers?.host;
const subdomain = host?.split(".")?.[0];
// console.log(subdomain);
</script>
