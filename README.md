[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/aMHx-K_k)
# 參考網址 : https://uniam.jp/
## 使用套件
### 一、 gsap
1. 安裝套件
``` npm i gsap```
2. 引入文件 (MainInfo4.vue)
```
import { onMounted } from 'vue'
import { gsap } from 'gsap'
```
3. 使用套件
```
export default {

  setup () {
    onMounted(() => {
      // 設定動畫
      gsap.to('#marquee1', {
        x: -1920, // 根據需要調整移動的距離
        duration: 20,
        repeat: -1, // 重複動畫
        ease: 'linear',
        modifiers: {
          x: (x) => {
            return parseFloat(x) < -1920 ? '1500' : x // 確保圖片循環
          }
        }
      })

      gsap.to('#marquee2', {
        x: -1920,
        duration: 20,
        repeat: -1,
        ease: 'linear',
        modifiers: {
          x: (x) => {
            return parseFloat(x) < -1920 ? '1500' : x
          }
        }
      })
    })
  }
}
```

### 二、 aox
1. 安裝
``` npm i aox ```
2. 引入文件 (MainInfo2.vue)
```
import AOS from 'aos'
import 'aos/dist/aos.css'
```
3. 使用套件，直接加在標籤裡
- data-aos 動畫樣式
- data-aos-easing 動畫速度曲線
- data-aos-duration 動畫持續時間(豪秒) 0~3000
- data-aos-delay 延遲幾秒撥放動畫 0~3000
- data-aos-offset 滾動多少像素後觸發動畫，預設120px
- data-aos-once 進場是否一次，false來回撥放動畫
### 三、 swiper 
1. 安裝
``` npm i swiper ```
2. 引入文件 (MainInfo3.vue)
```
import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css'
import 'swiper/css/autoplay'
import { Autoplay } from 'swiper/modules'
```
3. 使用套件
- slidesPerView：設置一次顯示的幻燈片數量(數字 or auto)
- spaceBetween：設置幻燈片之間的間距（以像素為單位）
- loop：是否開啟無限循環模式
- pagination：是否顯示分頁指示器
- navigation：是否顯示導航按鈕（上一頁和下一頁）
- autoplay：自動播放設置
- breakpoints：根據不同的視窗大小設置不同的屬性值
