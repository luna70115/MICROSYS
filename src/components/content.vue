<script setup lang="ts">
interface RecordItem {
  name: string;
  entryTime: string;
  exitTime: string;
  duration: string;
  cardNumber: string;
  image: string;
  class?: string; // 額外加的背景色 class，例如 "grey" 或 "pink"
}

const records: RecordItem[] = [
  {
    name: "丁小雨",
    entryTime: "2025/03/19 19:10",
    exitTime: "2025/03/19 19:10",
    duration: "00:30:00",
    cardNumber: "115030218",
    image: new URL("../assets/image/person1.jpg", import.meta.url).href,
  },
  {
    name: "丁小雨",
    entryTime: "2025/03/19 19:10",
    exitTime: "2025/03/19 19:10",
    duration: "00:30:00",
    cardNumber: "115030218",
    image: new URL("../assets/image/person2.jpg", import.meta.url).href,
    class: "grey",
  },
  {
    name: "丁小雨",
    entryTime: "2025/03/19 19:10",
    exitTime: "2025/03/19 19:10",
    duration: "00:30:00",
    cardNumber: "115030218",
    image: new URL("../assets/image/person3.jpg", import.meta.url).href,
    class: "pink",
  },
];
</script>

<template>
  <div class="content">
    <section class="statistics">
      <div class="statistics-card blue">
        <img src="../assets/image/user.png" alt="" />
        <p>今日人容數</p>
        <strong>0</strong>
      </div>
      <div class="statistics-card orange">
        <img src="../assets/image/warning.png" alt="" />
        <div>
          <p>今日累積</p>
          <p>末戴安全朝吹數</p>
        </div>
        <strong>0</strong>
      </div>
      <div class="statistics-card orange">
        <img src="../assets/image/warning.png" alt="" />
        <div>
          <p>今日累積</p>
          <p>危險显域警報次數</p>
        </div>
        <strong>0</strong>
      </div>
      <div class="statistics-card green">
        <img src="../assets/image/warning.png" alt="" />
        <div>
          <p>今日累積</p>
          <p>未戴安全帽次數</p>
        </div>
        <strong>0</strong>
      </div>
      <div class="statistics-card green">
        <img src="../assets/image/warning.png" alt="" />
        <div>
          <p>今日累積</p>
          <p>危險區域警報次數</p>
        </div>
        <strong>0</strong>
      </div>
    </section>
    <section class="proportion">
      <div class="proportion-card">
        <h2>場域人員佔比（矩形樹園）</h2>
        <img src="../assets/image/barChart.jpg" alt="" />
      </div>
      <div class="proportion-card">
        <h2>場域人員佔比（餅圖）</h2>
        <img src="../assets/image/pieChart.jpg" alt="" />
      </div>
    </section>
    <section class="log">
      <h2>紀錄</h2>
      <div class="log-card">
        <div class="log-tab">
          <p class="log-title">人臉辨識</p>
          <p class="log-title">姓名</p>
          <p class="log-title">進場時間</p>
          <p class="log-title">出場時間</p>
          <p class="log-title">滯留時間</p>
          <p class="log-title">聯安卡</p>
        </div>

        <ul v-for="(item, index) in records" :key="index" :class="item.class">
          <li><img :src="item.image" alt="" /></li>
          <li>
            <p class="log-text">{{ item.name }}</p>
          </li>
          <li>
            <p class="log-text">{{ item.entryTime }}</p>
          </li>
          <li>
            <p class="log-text">{{ item.exitTime }}</p>
          </li>
          <li>
            <p class="log-text">{{ item.duration }}</p>
          </li>
          <li>
            <p class="log-text">{{ item.cardNumber }}</p>
          </li>
        </ul>
      </div>
    </section>
    <section class="footer">
      <p></p>
      <p>Copyright • 2024 Microsys . All Rights Reserved. Microsys PPE</p>
      <img src="../assets/image/logo-big.png" alt="" />
    </section>
  </div>
</template>

<style lang="scss" scoped></style>
