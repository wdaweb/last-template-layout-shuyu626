<template>
  <v-app >
      <v-main>
        <router-view v-slot="{Component}" style="background-color: #FFF3E0;">
          <keep-alive include="index">
            <component :is="Component"></component>
          </keep-alive>
        </router-view>
      </v-main>
    </v-app>
  </template>

  <style>
    body{
      font-weight: bolder;
      font-family: "微軟正黑體";
      background-color: #FFF3E0;
    }

    .title-size{
    font-size: 13px;
  }
  .border-1{
    border: 1px solid black;
  }
  .border-bottom{
    border-bottom: 1px solid black;
  }

  </style>
