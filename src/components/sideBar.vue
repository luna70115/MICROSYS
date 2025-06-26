<script setup lang="ts">
import { ref } from "vue";

const isSubMenuOpen = ref<string | null>(null);

const toggleSubMenu = (tab: string) => {
  isSubMenuOpen.value = isSubMenuOpen.value === tab ? null : tab;
};
</script>

<template>
  <div class="side">
    <h2>MICROSYS</h2>
    <div class="side-card">
      <div class="side-box" @click="toggleSubMenu('dashboard')">
        <img src="../assets/image/speedometer.png" alt="" class="side-icon" />
        <p>儀表板</p>
        <img
          src="../assets/image/arrow.png"
          alt=""
          class="side-arrow"
          :class="{ 'side-arrow-rotate': isSubMenuOpen === 'dashboard' }"
        />
      </div>
      <ul v-show="isSubMenuOpen === 'dashboard'">
        <li>
          <p>儀表板</p>
          <img src="../assets/image/arrow.png" alt="" class="side-arrow" />
        </li>
      </ul>
      <div class="side-box" @click="toggleSubMenu('board')">
        <img src="../assets/image/kanban.png" alt="" class="side-icon" />
        <p>看板管理</p>
        <img
          src="../assets/image/arrow.png"
          alt=""
          class="side-arrow"
          :class="{ 'side-arrow-rotate': isSubMenuOpen === 'board' }"
        />
      </div>
      <ul v-show="isSubMenuOpen === 'board'">
        <li>
          <p>看板管理</p>
          <img src="../assets/image/arrow.png" alt="" class="side-arrow" />
        </li>
      </ul>
      <div class="side-box" @click="toggleSubMenu('material')">
        <img src="../assets/image/folder.png" alt="" class="side-icon" />
        <p>資料管理</p>
        <img
          src="../assets/image/arrow.png"
          alt=""
          class="side-arrow"
          :class="{ 'side-arrow-rotate': isSubMenuOpen === 'material' }"
        />
      </div>
      <ul v-show="isSubMenuOpen === 'material'">
        <li>
          <p>人員管理</p>
          <img src="../assets/image/arrow.png" alt="" class="side-arrow" />
        </li>
        <li>
          <p>車輛管理</p>
          <img src="../assets/image/arrow.png" alt="" class="side-arrow" />
        </li>
        <li>
          <p>日曆管理</p>
          <img src="../assets/image/arrow.png" alt="" class="side-arrow" />
        </li>
        <li>
          <p>出勤管理</p>
          <img src="../assets/image/arrow.png" alt="" class="side-arrow" />
        </li>
        <li>
          <p>門禁管理</p>
          <img src="../assets/image/arrow.png" alt="" class="side-arrow" />
        </li>
        <li>
          <p>資材管理</p>
          <img src="../assets/image/arrow.png" alt="" class="side-arrow" />
        </li>
        <li>
          <p>費用管理</p>
          <img src="../assets/image/arrow.png" alt="" class="side-arrow" />
        </li>
      </ul>
      <div class="side-box" @click="toggleSubMenu('teleport')">
        <img src="../assets/image/connection.png" alt="" class="side-icon" />
        <p>傳送管理</p>
        <img
          src="../assets/image/arrow.png"
          alt=""
          class="side-arrow"
          :class="{ 'side-arrow-rotate': isSubMenuOpen === 'teleport' }"
        />
      </div>
      <ul v-show="isSubMenuOpen === 'teleport'">
        <li>
          <p>傳送管理</p>
          <img src="../assets/image/arrow.png" alt="" class="side-arrow" />
        </li>
      </ul>
      <div class="side-box" @click="toggleSubMenu('permissions')">
        <img src="../assets/image/unlock.png" alt="" class="side-icon" />
        <p>權限管理</p>
        <img
          src="../assets/image/arrow.png"
          alt=""
          class="side-arrow"
          :class="{ 'side-arrow-rotate': isSubMenuOpen === 'permissions' }"
        />
      </div>
      <ul v-show="isSubMenuOpen === 'permissions'">
        <li>
          <p>權限管理</p>
          <img src="../assets/image/arrow.png" alt="" class="side-arrow" />
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
