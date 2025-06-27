<script setup lang="ts">
import SideBar from "./components/sideBar.vue";
import Header from "./components/header.vue";
import Content from "./components/content.vue";
import "./assets/styles/main.scss";
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
    margin-left: 20vw;
    overflow: auto;
    background-color: #e2f8ff;
  }
}
</style>
