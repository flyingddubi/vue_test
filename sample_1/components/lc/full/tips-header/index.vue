<script setup lang="ts">
import { ref } from 'vue';
// import { link } from 'fs';
// import { useI18n } from 'vue-i18n';

const items = ref([
  {
    title: "직무발명", link: "/tips_11", index: "1", depth: "0",
    sub_item: [{
      side_title: "출원진행", side_link: "/tips_11/tips_11_11", side_index: "1", depth: "1",
      children: [{ side_title_sub: "출원진행_sub1", side_depth: "2" },
      { side_title_sub: "출원진행_sub2", side_depth: "2" },
      { side_title_sub: "출원진행_sub3", side_depth: "2" },
      ]
    },
    {
      side_title: "종료관리", side_link: "/tips_11/tips_11_22", side_index: "2", depth: "1",
      children: [{ side_title_sub: "종료관리_sub1", side_depth: "2" },
      { side_title_sub: "종료관리_sub2", side_depth: "2" },
      { side_title_sub: "종료관리_sub3", side_depth: "2" },
      ]
    }]
  },
  { title: "비용관리", link: "/tips_22", index: "2", depth: "0" },
  { title: "현황관리", link: "/tips_33", index: "3", depth: "0" },
  { title: "기준관리", link: "/tips_44", index: "4", depth: "0" },
]);
</script>

<template>
    <div class="px-10 v-toolbar__content">

      <div class="nav smallCap text-uppercase text-subtitle-2 mt-5 font-weight-bold">
        <ul class="nav__list">
          <li class="nav__list__item" v-for="item in items">
            <!-- <nuxt-link :to = "item.link" @click="titleClick">{{ item.title }}</nuxt-link> -->
            <nuxt-link :to = "item.link">{{ item.title }}</nuxt-link>
          </li>
        </ul>
      </div>
    </div>
</template>

<style lang="scss" scoped>
.nav {
    display: flex;
    align-items: center;
    justify-content: center;

    width: 100%;
    margin-top: 15px;

    &__list {
        display: flex;
        align-items: center;
        justify-content: left;

        list-style: none;
        margin: 0;

        width: 100%;

        gap: 2px;

        &__item{
            display: flex;
            align-items: center;
            justify-content: center;
            align-self: flex-start;

            width: 100%;

            padding: 0;
            margin: 0 -4px 0 0;

            list-style: none;
            border: 2px solid black;

            &__title{
                // display: flex;
                align-items: center;
                justify-content: left;
                text-align: center;
                padding: 3px 6px;

                border: 1px solid black;

                background-color: white;}


            &__subtitle{
                display: flex;
                align-items: center;
                justify-content: left;

                padding: 5px 10px;

                border: 1px solid black;

                background-color: white;

            }
        }
    }
}
</style>
