<template>
<!--  <div>-->
<!--    <NuxtRouteAnnouncer />-->
<!--    <NuxtWelcome />-->
  <NuxtLayout>
    <AppHeader/>
    <NuxtPage/>
    <AppFooter/>
  </NuxtLayout>
<!--  </div>-->
</template>
<script setup lang="ts">
import AppHeader from "~/components/AppHeader.vue";
import AppFooter from "~/components/AppFooter.vue";
</script>