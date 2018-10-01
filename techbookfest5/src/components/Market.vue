<template>
  <div class="market">
      <h2 class="border">{{ name }}</h2>
      <div
              class="book"
              v-for="book in books"
              :key="book.name"
      >
          <img class="cover" :src="book.coverName" />
          <div class="detail">
              <h3>{{ book.name}}</h3>
              <div>
                  <p class="description">{{ book.description }}</p>
              </div>
              <ul
                      v-for="(chapter, i) in book.chapters"
                      :key="{ i }" >
                  <li>Chapter {{ i + 1 }}: {{ chapter.title }} - <a :href="'https://twitter.com/' + chapter.author">@{{ chapter.author }}</a></li>
              </ul>
          </div>
      </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
      return {
          name: "技術書典 5",
          books: [
              {
                  name: "Go & Kotlin Playground",
                  coverName: "go-and-kotlin-playground.png",
                  description: "Go アプリケーションに関する設計や、Go 製ツールの話、Kotlin のチートシートなど、GCF メンバーそれぞれの知見集です。",
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
  }
}
</script>

<style scoped>
    @font-face {
        src: url("/fonts/nexa-bold.otf") format("otf"), url("/fonts/nexa-light.otf") format("otf");
    }
  .cover {
      width: 30%;
      height: 30%;
  }

    .market {
        padding: 0 13vw;
        font-family: Helvetica, Arial, sans-serif;
    }

    .book {
        display: flex;
        align-items: center;
    }

    .detail {
        width: 95%;
        padding-left: 5%;
        text-align: left;
    }

    .market > h2 {
        font-size: 1.8rem;
        color: #333;
    }

    .detail > h3 {
        font-family: "Nexa Bold";
        font-size: 3rem;
        color: #232a53;
    }

    ul {
        padding-left: 3%;
    }

    li {
        list-style: none;
    }

    .description {
        margin-bottom: 5%;
    }

    .border {
        display: flex;
        align-items: center;
    }

    .border::before,
    .border::after {
        border-top: 1px solid #ccc;
        content: '';
        flex-grow: 1;
    }

    .border::before {
        margin-right: 1.5rem;
    }

    .border::after {
        margin-left: 1.5rem;
    }
</style>
