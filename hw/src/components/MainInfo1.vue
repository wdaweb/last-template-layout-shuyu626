<template>
      <section id="section2" class="border-bottom bg-orange-lighten-5">
          <v-row class="text-center my-5 mt-md-12" >
            <v-col cols="6" md="3" class="my-auto" >
              <img src="@/assets/section2/nikkei_design_logo.webp" alt="">
            </v-col>
            <v-col cols="6" md="3" class="my-auto">
              <img src="@/assets/section2/nikkei_xtrend_logo.avif" alt="">
            </v-col>
            <v-col cols="6" md="3" class="my-auto">
              <img src="@/assets/section2/and-premium_logo.avif" alt="">
            </v-col>
            <v-col cols="6" md="3" class="my-auto">
              <img src="@/assets/section2/nekonokimochi_logo.avif" alt="">
            </v-col>
          </v-row>
      </section>
      <section id="section3" class="border-bottom">
        <v-img src="@/assets/section3/top_newproduct_banner_pc.webp"></v-img>
      </section>
</template>
<style scoped>
#section2{
  width: 100vw;
  @media (min-width: 1280px) {
        height: 18vh;
  }
  img{
    width: 200px;
  }
}
#section3{
  width: 100vw;
}
</style>
