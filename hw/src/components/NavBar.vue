<template>
     <v-app-bar height="70" elevation="0" class="border-bottom " style="background-color:#97CBB8;" >
        <v-icon class="ml-2">mdi-volume-high</v-icon>
        <v-app-bar-title class="font-weight-black text-body-1">税込10,000円以上のお買い物で送料無料</v-app-bar-title>
        <v-icon class="me-lg-6">mdi-chevron-right</v-icon>
      </v-app-bar>
      <v-app-bar color="orange-lighten-5" elevation="0" class="border-bottom navbar">
          <v-row class="mt-lg-1">
            <v-col cols="4">
              <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
              <span v-if="!mobile">
                <v-btn class="text-md-body-1 font-weight-bold">商品一覧</v-btn>
                <v-btn class="text-md-body-1 font-weight-bold">ユニアムの特徴</v-btn>
                <v-btn class="text-md-body-1 font-weight-bold">ねこの方はこちら</v-btn>
                <v-btn class="text-md-body-1 font-weight-bold">開発ストーリー</v-btn>
              </span>
            </v-col>
            <v-col cols="4"  class="text-center my-auto">
              <v-app-bar-title>
              <img src="@/assets/icon/en01.png" width="80" >
            </v-app-bar-title>
            </v-col>
            <v-col  cols="4"  class="text-right my-auto">
              <v-icon class="mx-2">mdi-account</v-icon>
              <v-icon class="mr-2">mdi-cart-variant</v-icon>
            </v-col>
          </v-row>
      </v-app-bar>
      <v-navigation-drawer  v-model="drawer" color="blue-accent-3" >
        <v-list>
          <v-btn variant="text" class="my-3" @click="drawer = !drawer" >x 閉じる</v-btn>
          <v-list-item title="商品一覧"></v-list-item>
          <v-divider></v-divider>
          <v-list-item>FOOD SERIES</v-list-item>
          <v-divider></v-divider>
          <v-list-item>フレッシュフードの特徴</v-list-item>
          <v-divider></v-divider>
          <v-list-item>ねこの方はこちら</v-list-item>
          <v-divider></v-divider>
          <v-list-item>開発ストーリー</v-list-item>
          <v-divider></v-divider>
          <v-list-item>レビュー</v-list-item>
          <v-divider></v-divider>
        </v-list>
      </v-navigation-drawer>
</template>
<script setup>
import { ref } from 'vue'
import { useDisplay } from 'vuetify'
const drawer = ref(false)
const { mobile } = useDisplay()
</script>
<style>
   .title-size{
    font-size: 13px;
  }
  .border-1{
    border: 1px solid black;
  }
  .border-bottom{
    border-bottom: 1px solid black;
  }
  .navbar{
    @media (min-width: 1280px) {
        height: 9vh;
    }
  }

</style>
