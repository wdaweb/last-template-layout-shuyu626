<template>
    <v-footer id="footer" class="bg-transparent " >
      <v-container>
        <v-row class="flex-column flex-lg-row align-start justify-center mx-auto" >
          <v-col>
            <v-row class=" flex-lg-column">
              <v-col class="text-lg-h6">Contents</v-col>
              <v-col>
                <a href="#"><li>トップページ</li></a>
                <a href="#"><li>レシピについて</li></a>
                <a href="#"><li>ユニアムの特徴</li></a>
                <a href="#"><li>レビュー</li></a>
                <a href="#"><li>ユニアムクラブ</li></a>
                <a href="#"><li>はじめてガイド</li></a>
                <a href="#"><li>開発ストーリー</li></a>
                <a href="#"><li>ねこの方はこちら</li></a>
              </v-col>
            </v-row>
          </v-col>
          <v-col>
            <v-row  class=" flex-lg-column">
              <v-col></v-col>
              <v-col>
                <a href="#"><li>会社概要</li></a>
                <a href="#"><li>よくあるご質問</li></a>
                <a href="#"><li>利用規約</li></a>
                <a href="#"><li>特定商取引法について</li></a>
                <a href="#"><li>プライバシーポリシー</li></a>
              </v-col>
            </v-row>
          </v-col>
          <v-col>
            <v-row  class=" flex-lg-column">
              <v-col class="text-lg-h6">Official SNS</v-col>
              <v-col>
                <a href="#">
              <li>
                <v-btn
                variant="text"
                prepend-icon="mdi-instagram"
                max-height="20"
                >instagram</v-btn>
              </li>
            </a>
            <a href="#">
              <li>
                <v-btn
                variant="text"
                prepend-icon="mdi-twitter"
                max-height="20"
                >X</v-btn>
              </li>
            </a>
            <a href="#">
              <li>
                <v-btn
                variant="text"
                prepend-icon="mdi-facebook"
                max-height="20"
                >Facebook</v-btn>
              </li>
            </a>
            <a href="#">
              <li>
                <v-btn
                variant="text"
                prepend-icon="mdi-note"
                max-height="20"
                >note</v-btn>
              </li>
            </a>
              </v-col>
            </v-row>
          </v-col>
          <v-col>
            <v-row class=" flex-lg-column">
              <v-col class="text-lg-h6">Contact</v-col>
              <v-col>
                <a href="#"><li style="text-decoration: underline;">meow@uniam.jp</li></a>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </v-footer>
</template>
<script>
export default {
  name: 'AppFooter'
}
</script>
<style scoped>
#footer{
  height: 80vh;
  a{
    text-decoration: none;
    color: black;
    li{
      list-style: none;
      font-size: 13px;
      margin-bottom: 7px;
    }
  }

}
</style>
