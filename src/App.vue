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
                "Go アプリケーションに関する設計や、Go 製ツールの話、Kotlin のチートシートなど、GCF メンバーそれぞれの知見集です。",
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
  margin-top: 60px;
}
</style>
