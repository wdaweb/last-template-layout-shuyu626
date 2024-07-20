<template>
    <section id="section7" class="border-bottom ">
        <v-container>
          <v-row class="mx-3 my-lg-8">
            <v-col cols="12" md="6" lg="3" class="text-lg-h5">
              <h4 class="font-weight-bold">ねこの身体特性に基づいた</h4>
              <h3 class="font-weight-bold">国産の無添加フード</h3>
              <p class="text-body-2 my-2 font-weight-bold text-lg-body-1">肉食動物のねこのために、高品質なお肉とお魚を贅沢に使用。良質なタンパク質で毎日の健康をサポート。</p>
            </v-col>
            <v-col cols="12" md="6" lg="3">
              <v-card variant="outlined" class="bg-white">
                <span class="mx-3 my-3 border-1 bg-white">総合栄養食</span>
                <v-img src="@/assets/section7/fresh_bc_main.webp" ></v-img>
                <v-card-subtitle>冷凍フレッシュフード</v-card-subtitle>
                <v-card-text>ユニアムの定番。<br>
                国産食材をやさしく低温調理した総合栄養食。<br>¥3,310/税込</v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" md="6" lg="3">
              <v-card variant="outlined" class="bg-white">
                <span class="mx-3 my-3 border-1">総合栄養食</span>
                <v-img src="@/assets/section7/top_lineup_puree.webp"></v-img>
                <v-card-subtitle>冷凍フレッシュフード</v-card-subtitle>
                <v-card-text>ユニアムの定番。<br>国産食材をやさしく低温調理した総合栄養食。<br>¥3,310/税込〜</v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" md="6" lg="3">
              <v-card variant="outlined" class="bg-white">
                <span class="mx-3 my-3 border-1">総合栄養食</span>
                <v-img src="@/assets/section7/wildsnack-set_main_transparent.webp"></v-img>
                <v-card-subtitle>ワイルドスナック</v-card-subtitle>
                <v-card-text>添加物無添加。素材そのまま、<br>
                  自然環境の食事でねこ本来の健康的な体つきへ。<br>¥
                  800/税込〜
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </v-container>
      </section>
      <section id="section8" class="bg-deep-purple-lighten-4 text-center py-12 border-bottom">
        <h2>ねこたちのごきげんな声</h2>
        <h3 class="my-2">@uniam_official</h3>
        <div>
          <swiper
            :modules="modules"
            :pagination="{ clickable: true }"
            :loop="true"

            :autoplay="{ delay: 1000, disableOnInteraction: true }"
            class="my-8"
            ref="mySwiper"
            :breakpoints="{
              '480': {
                slidesPerView: 3,
                spaceBetween: 30
              },
              '1024': {
                slidesPerView: 6,
                spaceBetween: 30
              }
            }"
          >
            <swiper-slide v-for="slide in slides" :key="slide.id">
              <v-img :src="slide.image" style="border: 1px solid #000" width="250px"></v-img>
            </swiper-slide>
          </swiper>
        </div>
        <div>
          <swiper
            :modules="modules"
            :pagination="{ clickable: true }"
            :loop="true"

            :autoplay="{ delay: 1000, disableOnInteraction: true, reverseDirection: true }"
            ref="mySwiper2"
            :breakpoints="{
              '480': {
                slidesPerView: 3,
                spaceBetween: 30
              },
              '1024': {
                slidesPerView: 6,
                spaceBetween: 30
              }
            }"
          >
            <swiper-slide v-for="sli in slides2" :key="sli.id">
              <v-img :src="sli.image" style="border: 1px solid #000" width="250px"></v-img>
            </swiper-slide>
          </swiper>
        </div>
      </section>
      <section id="section9" class="border-bottom ">
        <v-container>
          <h3 class="my-2 text-lg-h4 font-weight-bold">ユニアムの「3つの特徴」</h3>
          <p class="text-body-2 text-lg-h6 font-weight-bold">ねこ専門のユニアムだから、</p>
          <p class="text-body-2 text-lg-h6 font-weight-bold">ねこの幸せだけをとことん追求。</p>
        </v-container>
      </section>
</template>
<script>
import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css'
import 'swiper/css/autoplay'
import 'swiper/css/navigation'
import 'swiper/css/pagination'
import { Autoplay } from 'swiper/modules'

export default {
  components: {
    Swiper,
    SwiperSlide
  },
  setup () {
    const modules = [Autoplay]
    const slides = [
      { id: 1, image: new URL('@/assets/section8/catsloop_line1_1.avif', import.meta.url).href },
      { id: 2, image: new URL('@/assets/section8/catsloop_line1_2.avif', import.meta.url).href },
      { id: 3, image: new URL('@/assets/section8/catsloop_line1_3.webp', import.meta.url).href },
      { id: 4, image: new URL('@/assets/section8/catsloop_line1_5.avif', import.meta.url).href },
      { id: 5, image: new URL('@/assets/section8/catsloop_line1_6.avif', import.meta.url).href },
      { id: 6, image: new URL('@/assets/section8/catsloop_line2_1.avif', import.meta.url).href },
      { id: 7, image: new URL('@/assets/section8/catsloop_line1_5.avif', import.meta.url).href }
    ]
    const slides2 = [
      { id: 1, image: new URL('@/assets/section8/catsloop_line2_2.avif', import.meta.url).href },
      { id: 2, image: new URL('@/assets/section8/catsloop_line2_3.avif', import.meta.url).href },
      { id: 3, image: new URL('@/assets/section8/catsloop_line2_4.avif', import.meta.url).href },
      { id: 4, image: new URL('@/assets/section8/catsloop_line2_6.avif', import.meta.url).href },
      { id: 5, image: new URL('@/assets/section8/catsloop_line1_1.avif', import.meta.url).href },
      { id: 6, image: new URL('@/assets/section8/catsloop_line1_2.avif', import.meta.url).href },
      { id: 7, image: new URL('@/assets/section8/catsloop_line1_3.webp', import.meta.url).href }
    ]

    return { slides, slides2, modules }
  }
}

</script>
<style scoped>
#section7{
  width: 100vw;
  /* height: 170vh; */
    span{
      border-radius: 20px;
      padding:4px;
      font-size: 13px;
      width: 95px;
      display: inline-block;
      text-align: center;
      padding: 2px;
    }
  }

#section8{
  height: 80vh;
    .swiper img{
      width: 100%;
    object-fit: contain;
    }
  }
#section9{
  height: 55vh;
  background: url("@/assets/section9/feature_foodforcats_main.webp");
  background-size:cover;
  background-repeat: no-repeat;
  background-position: center center;
}
</style>
