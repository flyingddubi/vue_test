<script setup lang="ts">
import TipsHeader from "~/\bcomponents/tips-header/tips-header.vue";
import VerticalSidebar from "~/\bcomponents/vertical-sidebar/vertical-sidebar.vue";
</script>

<template>
  <div style="border: 2px solid red">
    <h1>헤더입니다.</h1>
    <TipsHeader @layoutFunc="layoutFunc" />
  </div>
  <div>
    <h1>레이아웃입니다..</h1>
    <h2>layout data: {{ layoutData }}</h2>
  </div>
  <div>
    <h1>사이드바입니다.</h1>
    <VerticalSidebar :verticalSidebarData="layoutData" />
  </div>
</template>

<style scoped></style>

<script lang="ts">
export default {
  data() {
    return {
      layoutData: "layout",
    };
  },
  methods: {
    layoutFunc(data: string) {
      this.layoutData = data;
    },
  },
};
</script>
