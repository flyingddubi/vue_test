<script setup lang="ts">
import { useRoute } from "vue-router";
import { ref } from 'vue';

const items = ref([
  { message : "출원진행", link : "/tips_11/tips_11_11" },
  { message : "종료관리", link : "/tips_11/tips_11_22" },
])

</script>

<template>
      <div class="sidebar">
        <v-list class="pa-6" density="compact">
          <ul>
            <li v-for="item in items" ><nuxt-link to = "/">{{ item.message }}</nuxt-link></li>
          </ul>    
        </v-list>
      </div>
</template>

<style>
.item {
  cursor: pointer;
  line-height: 1.5;
}
.bold {
  font-weight: bold;
}

/* .sidebar {
  
  position: fixed;
  top: 110px;
  left: 0;
  height: 100%;
  width: 200px;

  margin:0 !important;
  z-index: 1000;
  display: flex;

  border: 2px solid red;
  background-color: white;
} */
</style>