<template>
  <div class="container">
    <h1>DESIGNS</h1>
    <article>
      <section>
        <h2>WEB</h2>
        <h3>WEBのデザイン</h3>
        <p>
          バナー類全般をはじめとして、ロゴやアイコン、サイトデザインの経験があります。WEBバナー系の制作が最も多く、ECサイト訴求画像ではその多くが
          amazon / yahoo / 楽天 で売上1位を達成しています。<br />ロゴに関してはフリーでお仕事を頂き始めた当初、ロゴコンペ【採用】ランキングにて、2017年04月第3週：第1位
          / 2017年04月月間：第7位を獲得しました。<br />バナーやロゴ類よりも件数自体は少ないですが、サイトデザイン・LPデザインも受注経験があり、好評を頂いています。なおこのサイトのデザインはAdobe
          XDにて制作しております。
        </p>
        <ul class="examples">
          <li v-for="example in web.examples" :key="example.title">
            <a v-bind:href="example.path"
              ><span>{{ example.title }}</span></a
            >
          </li>
        </ul>
        <ul class="keywords">
          <li v-for="keyword in web.keywords" :key="keyword">
            {{ keyword }}
          </li>
        </ul>
      </section>
      <section>
        <h2>EDITORIAL</h2>
        <h3>紙のデザイン</h3>
        <p>
          チラシ・フライヤー・パッケージからCDジャケット・オリジナルグッズデザイン等の印刷物デザインが可能です。制作物によりますが、ご希望により印刷業者への入稿まで対応しています。変わったご依頼としては、イラスト制作・大型看板の制作などの経験があります。
        </p>
        <ul class="examples">
          <li v-for="example in editorial.examples" :key="example.title">
            <a v-bind:href="example.path" target="_blank"
              ><span>{{ example.title }}</span></a
            >
          </li>
        </ul>
        <ul class="keywords">
          <li v-for="keyword in editorial.keywords" :key="keyword">
            {{ keyword }}
          </li>
        </ul>
      </section>
    </article>
    <footer>
      <p>
        © Copyright 2019 │ Masayoshi Kawashima a.k.a. ma-ya’s CREATE All rights
        reserved.
      </p>
    </footer>
  </div>
</template>

<script>
export default {
  name: "designs",
  data() {
    return {
      web: {
        examples: [
          {
            title: "WEBサイト「Charlotte is Mine – official website」",
            path: "https://myscreate.com/gallery/websites-3/",
          },
          {
            title: "EC訴求画像「GACHILOCK」",
            path: "https://myscreate.com/gallery/graphics-2/",
          },
          {
            title: "ロゴ「F channel」",
            path: "https://myscreate.com/gallery/logos-2/",
          },
        ],
        keywords: [
          "photoshop",
          "illustrator",
          "Adobe XD",
          "premiere pro",
          "ECサイト",
          "WEBサイト",
          "LP",
          "ロゴ",
          "バナー",
        ],
      },
      editorial: {
        examples: [
          {
            title: "商品パッケージ「ELECTIVE CHARGER」",
            path: "https://myscreate.com/gallery/printed-matter/",
          },
          {
            title: "ウォールアート「SUMMER BALL 2018」",
            path: "https://myscreate.com/gallery/printed-matter-3/",
          },
          {
            title: "名刺「Kii Point Inc.」",
            path: "https://myscreate.com/gallery/printed-matter-2/",
          },
        ],
        keywords: [
          "photoshop",
          "illustrator",
          "DTP",
          "パッケージ",
          "フライヤー",
          "ポスター",
          "看板",
          "CDジャケット",
          "グッズ",
          "イラスト",
          "名刺",
        ],
      },
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/common.scss";
</style>