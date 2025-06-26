<script setup lang="ts">
import { ref } from "vue";

const getFormattedDateTime = () => {
  const now = new Date();

  const year = now.getFullYear();
  const month = String(now.getMonth() + 1).padStart(2, "0");
  const day = String(now.getDate()).padStart(2, "0");

  const hours = String(now.getHours()).padStart(2, "0");
  const minutes = String(now.getMinutes()).padStart(2, "0");
  const seconds = String(now.getSeconds()).padStart(2, "0");

  return `${month}/${day}/${year} ${hours}-${minutes}:${seconds}`;
};

// 💡 正確宣告方式：呼叫函式並儲存
const currentTime = ref(getFormattedDateTime());
</script>

<template>
  <div class="header">
    <div>
      <img src="../assets/image/hamburger.png" alt="" />
      <p>儀表板</p>
    </div>
    <div>
      <p>當前時間：{{ currentTime }}</p>
      <img src="../assets/image/frame.png" alt="" />
      <img src="../assets/image/earth-globe.png" alt="" />
      <img src="../assets/image/profile.png" alt="" />
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
