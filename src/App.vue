<script setup lang="ts">
import SideBar from "./components/sideBar.vue";
import Header from "./components/header.vue";
import Content from "./components/content.vue";

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
  <div class="main">
    <SideBar></SideBar>
    <div class="main-content"><Header></Header> <Content></Content></div>
  </div>
</template>

<style lang="scss">
.main {
  display: flex;
  &-content {
    display: flex;
    flex-direction: column;
    flex: 1;
    width: 100%;
    height: 100vh;
    overflow: auto;
    background-color: #e2f8ff;
  }
}
</style>
