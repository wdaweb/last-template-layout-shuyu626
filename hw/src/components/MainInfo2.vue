<template>
    <section id="section4" class="bg-deep-purple-lighten-4 border-bottom">
        <v-container class="text-center">
          <h3 class="my-4 mb-8  text-lg-h4">COMING SOON</h3>
          <v-row class="mx-lg-8">
            <v-col cols="6" lg="3" >
              <img src="@/assets/section4/newin_3.avif" class="w-lg-75"  data-aos="fade-up" data-aos-duration="3000">
            </v-col>
            <v-col cols="6" lg="3" >
              <img src="@/assets/section4/newin_1.avif" class="w-lg-75"  data-aos="fade-up" data-aos-duration="3000">
            </v-col>
            <v-col cols="6" lg="3" >
              <img src="@/assets/section4/newin_2.avif" class="w-lg-75"  data-aos="fade-up" data-aos-duration="3000">
            </v-col>
            <v-col cols="6" lg="3" >
              <img src="@/assets/section4/newin_4.webp" class="w-lg-75"  data-aos="fade-up" data-aos-duration="3000">
            </v-col>
          </v-row>
          <div class="text-left ml-7">
            <h4 class="mt-5 text-lg-h4">Newsletter</h4>
            <p class="text-body-2  text-lg-h6">ニュースレター</p>
            <br>
            <p class="text-body-2 text-lg-h6">LINEで友だち登録をすると、送料無料クーポンをプレゼント！
              限定クーポンや新商品のご案内など、おトクな情報を発信していきます。</p>
          </div>
          <v-btn class="my-5 rounded-lg text-body-2 font-weight-bold" elevation="0" height="50" variant="flat">LINEでお友達登録</v-btn>
        </v-container>
      </section>
      <section id="section5" class="border-bottom">
        <v-container>
          <div class="ml-7 my-5">
            <v-row >
              <v-col cols="12" lg="6" class="text-lg-center text-lg-h4 mt-lg-10">
                <h3 class="font-weight-black" data-aos="slide-right" data-aos-delay="2000">ねこと生きるを、</h3>
                <h3 class="font-weight-black" data-aos="slide-right" data-aos-delay="2000">ユニークに。</h3>
              </v-col>
            <br>
            <br>
            <v-col cols="12" lg="6" class=" text-lg-left mt-lg-10 ">
              <div data-aos="slide-right" data-aos-delay="2500">
                <p class="text-lg-h6">自由気ままで、甘えん坊。<br>
                小さなからだに、大きな振る舞い。<br>
                奔放でかわいいねこたちは、<br>
                そこにいるだけでほころぶような幸せを、<br>
                いつもくれている。<br>
            </p>
            <br>
            <p class="text-lg-h6">
              それなのに、ねこを取り巻く環境は、<br>
              ヒトの常識にとらわれている。<br>
              わたしたちは、<br>
              そんな世界を変えていきたいのです。<br>
            </p>
            <br>
            <p class="text-lg-h6">
              「そういうものだから」と野放しに<br>
              なってきたことを、ひとつひとつ疑う。<br>
              どんなに大きな課題にだって、<br>
              わたしたちにしか生み出せない答えを。<br>
            </p>
            <br>
            <p class="text-lg-h6">
              専門家の知見とクリエイティビティを<br>
              かけあわせ、ねこを愛するヒトビトに、<br>
              その隣でぐうぐう眠るねこたちに、<br>
              まだこの世界にない、<br>
              ユニークなアイディアを届けていきます。
            </p>
              </div>

            <img id="neko"  src="@/assets/cat_stretch_green.webp">
            </v-col>
          </v-row>
        </div>
      </v-container>
      </section>
      <section id="section6" class="border-bottom" >
        <v-container>
          <h1>
            主食からおやつまで<br>
            Food Series
          </h1>
        </v-container>
      </section>
</template>
<script>
import { onMounted } from 'vue'
import AOS from 'aos'
import 'aos/dist/aos.css'
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'
gsap.registerPlugin(ScrollTrigger)
AOS.init({
  once: true
})

onMounted(async () => {
  gsap.to('#neko', {
    scrollTrigger: {
      trigger: '#neko',
      markers: true, // 紅綠線標記
      start: 'center bottom', // 綠色線
      end: 'center bottom' // 紅色線
    },
    x: 750,
    duration: 1,
    ease: 'ease-in'
  })
})
</script>
<style scoped>
#section4{
  width: 100vw;
  /* height: 85vh; */
  img{
    width: 43vw;
    border: 1px solid black;
  }
}
#section5{
  width: 100vw;
  height: 85vh;
  position: relative;
  #neko{
    position: absolute;
    bottom: 0%;
    left: 10%;
    height: 13vh;
  }
  p{
    font-size: 14px;
  }
}
#section6{
  width: 100vw;
  height: 50vh;
  background: url("@/assets/section6/top_sec_food_pc.webp");
  background-size: cover;
  background-position: center bottom;
}
</style>
