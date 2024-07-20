<template>
    <section id="section1" class=" bg-orange-lighten-5">
      <swiper
        :modules="modules"
        :slides-per-view="1"
        :space-between="0"
        :loop="true"
        :autoplay="{
          delay: 3000,
          disableOnInteraction: false,
        }"

        @swiper="onSwiper"
        @slideChange="onSlideChange"
        ref="mySwiper"
      >
        <swiper-slide>
          <img src="@/assets/section1/lifestyle_teaser_kv_1_sp.webp" class="img_about">
          <img id="icon" src="@/assets/icon/en01.png" width="500" class="my-7 mx-auto">
          <div class="swiper_text text-lg-h5">
            <p>獣医師・栄養士監修</p>
            <p>ねこ専門のフレッシュフード</p>
          <v-btn id="btn" class="my-5 mb-12 rounded-pill bg-orange-darken-3 text-body-1 font-weight-black" elevation="0" width="190" height="60">今すぐ無料診断</v-btn>
          </div>

        </swiper-slide>
        <swiper-slide >
          <img src="@/assets/section1/lifestyle_teaser_kv_5_sp.webp" class="img_about">
          <img id="icon" src="@/assets/icon/en01.png" width="500" class="my-7 mx-auto">
          <div class="swiper_text text-lg-h5">
            <p>獣医師・栄養士監修</p>
            <p>ねこ専門のフレッシュフード</p>
          <v-btn id="btn" class="my-5 mb-12 rounded-pill bg-orange-darken-3 text-body-1 font-weight-black" elevation="0" width="190" height="60">今すぐ無料診断</v-btn>
          </div>
        </swiper-slide>
        <swiper-slide>
          <img src="@/assets/section1/lifestyle_teaser_kv_3_sp.webp" class="img_about">
          <img id="icon" src="@/assets/icon/en01.png" width="500" class="my-7 mx-auto">
          <div class="swiper_text text-lg-h5">
            <p>獣医師・栄養士監修</p>
            <p>ねこ専門のフレッシュフード</p>
          <v-btn id="btn" class="my-5 mb-12 rounded-pill bg-orange-darken-3 text-body-1 font-weight-black" elevation="0" width="190" height="60">今すぐ無料診断</v-btn>
          </div>
        </swiper-slide>
        <swiper-slide>
          <img src="@/assets/section1/lifestyle_teaser_kv_4_sp.webp" class="img_about">
          <img id="icon" src="@/assets/icon/en01.png" width="500" class="my-7 mx-auto">
          <div class="swiper_text text-lg-h5">
            <p>獣医師・栄養士監修</p>
            <p>ねこ専門のフレッシュフード</p>
          <v-btn id="btn" class="my-5 mb-12 rounded-pill bg-orange-darken-3 text-body-1 font-weight-black" elevation="0" width="190" height="60">今すぐ無料診断</v-btn>
          </div>
        </swiper-slide>
      </swiper>
    </section>
  </template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css'
import 'swiper/css/autoplay'
import { Autoplay } from 'swiper/modules'

export default {
  components: {
    Swiper,
    SwiperSlide
  },
  setup () {
    const onSwiper = (swiper) => {
      console.log(swiper)
    }
    const onSlideChange = () => {
      console.log('slide change')
    }
    const modules = [Autoplay]
    return {
      onSwiper,
      onSlideChange,
      modules
    }
  },
  mounted () {
    this.$nextTick(() => {
      const swiper = this.$refs.mySwiper.swiper
      if (swiper && swiper.params) {
        swiper.params.autoplay = {
          delay: 4000,
          disableOnInteraction: false
        }
        swiper.autoplay.start()
      }
    })
  }
}
</script>

<style scoped>
#section1{
  width: 100vw;
  height: 90vh;
  overflow: hidden;
  #icon{
    position: absolute;
    top: 10%;
    left: 50%;
    transform: translate(-50%,-10%);
    width: 200px;
    z-index: 10;

  }
  .swiper{
    height: 100%;
  }
  .swiper_text{
    text-align: center;
    position: absolute;
    top: 90%;
    left: 50%;
    transform: translate(-50%,-90%);
    font-weight: bold;
  }
  .swiper-slide{
    text-align: center;
  }
  .img_about{
    width: 100%;
    height: 100%;
    /* object-position: center; */
    object-fit: cover;
  }

}
</style>
