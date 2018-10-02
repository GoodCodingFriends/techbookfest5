<template>
  <div id="app">
    <h1>GCF Lab</h1>
    <Market
            v-for="market in markets"
            :key="market.name"
            :market="market" />
  </div>
</template>

<script>
import Market from "./components/Market.vue";
import Media from "vue-media";

export default {
  name: "app",
  components: {
    Market,
    Media
  },
  data() {
    return {
      markets: [
        {
          name: "技術書典 5",
          place: "う11",
          url: "//techbookfest.org/event/tbf05/circle/26840001",
          books: [
            {
              name: "Go & Kotlin Playground",
              coverName: "go-and-kotlin-playground.png",
              description:
                "Go と Kotlin に関する本です。Go アプリケーション設計や、Go 製ツールの話、Docker、Kotlin のチートシートなど、GCF メンバーそれぞれの知見を集めています。",
              chapters: [
                {
                  title: "gRPC Web Internals",
                  author: "ktr_0731"
                },
                {
                  title: "やはり俺の Go アプリケーション設計はまちがっている。",
                  author: "ktr_0731"
                },
                {
                  title: "FUSE で HackMD FS を作って完璧なメモ環境を整える",
                  author: "acomagu"
                },
                {
                  title:
                    "go-ethereum が入っているアプリケーションを Docker コンテナにしたい",
                  author: "Yamashou0314"
                },
                {
                  title:
                    "私が調べた Images API で生成される Serving URL の画像機能チートシート",
                  author: "Yamashou0314"
                },
                {
                  title: "My Kotlin Cheat Sheet",
                  author: "slme_not_found"
                }
              ]
            }
          ]
        }
      ]
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 60px auto;
}
</style>
