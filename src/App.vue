<script setup lang="ts">
import "./assets/styles/main.scss";

const now = new Date();

function formatCustomDate(date: Date): string {
  const pad = (n: number) => n.toString().padStart(2, "0");

  const month = pad(date.getMonth() + 1);
  const day = pad(date.getDate());
  const year = date.getFullYear();

  const hours = pad(date.getHours());
  const minutes = pad(date.getMinutes());
  const seconds = pad(date.getSeconds());

  return `${month}/${day}/${year} ${hours} ${minutes}:${seconds}`;
}

const formattedNow = formatCustomDate(now);
</script>

<template>



   

</template>

<style lang="scss">

</style>