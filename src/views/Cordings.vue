<template>
  <div class="container">
    <h1>CORDINGS</h1>
    <article>
      <section>
        <h2>HTML5 / CSS3</h2>
        <h3>マークアップ / レイアウト / CSSアニメーション</h3>
        <p>
          WEBサイトのデザイン→コーディングまでをワンストップで行います。HTML5によるHTML構造はSEOの根本を担う部分と考えているため、セマンティックな構造を意識しています。またCSS3で豊かになったアニメーションを駆使して様々な表現を試みることが好きで、CodePenやポートフォリオでのブログによる発信で日々アウトプットを行っています。CSSは主にSass（SCSS）、最近はHTML記述にPugを試しています。
        </p>
        <ul class="examples">
          <li v-for="example in markup.examples" :key="example.title">
            <a v-bind:href="example.path"
              ><span>{{ example.title }}</span></a
            >
          </li>
        </ul>
        <ul class="keywords">
          <li v-for="keyword in markup.keywords" :key="keyword">
            {{ keyword }}
          </li>
        </ul>
      </section>
      <section>
        <h2>JS</h2>
        <h3>Javascript / jQuery / Vue.js</h3>
        <p>
          スクロール、クリックイベントなど主にサイト上のインタラクション /
          UI実装にJSを使用しております。プラグインを使用することもありますが、基本的には自身のコードで実現できるよう努めています。<br />jQueryに関してはちょっとしたプラグインも制作しており、CodePenでデモをピックアップして頂きました。また最近ではVue.jsへの興味から独学を進めており、ブログで入門記事を発信しています。<br />なおこのサイトはVue.jsによるSPAとして制作しており、Vue
          CLIによってビルド環境を構築しました。
        </p>
        <ul class="examples">
          <li v-for="example in js.examples" :key="example.title">
            <a v-bind:href="example.path" target="_blank"
              ><span>{{ example.title }}</span></a
            >
          </li>
        </ul>
        <ul class="keywords">
          <li v-for="keyword in js.keywords" :key="keyword">
            {{ keyword }}
          </li>
        </ul>
      </section>
      <section>
        <h2>PHP-WordPress</h2>
        <h3>ワードプレス（PHP）</h3>
        <p>
          WordPressは既存テーマのカスタマイズはもちろん、PHPによる独自テーマの制作経験があります。ポートフォリオ本サイトを独自テーマ化し、それを気に入って頂いたクライアント様のサイトをXAMPP仮想環境にて制作したこともありました。PHPはWordPressの範囲で触れるのみですが、サーバーサイド言語習得の必要性も強く感じる為、少しずつRubyの独学も始めようと考えています。
        </p>
        <ul class="examples">
          <li v-for="example in php.examples" :key="example.title">
            <a v-bind:href="example.path" target="_blank"
              ><span>{{ example.title }}</span></a
            >
          </li>
        </ul>
        <ul class="keywords">
          <li v-for="keyword in php.keywords" :key="keyword">
            {{ keyword }}
          </li>
        </ul>
      </section>
      <section>
        <h2>Environment</h2>
        <h3>総合環境</h3>
        <p>
          総合的な環境は以下となります。ソース管理は個人の範囲ではありますが Git
          / GitHub にて管理しております。<br />CodePenはコンポーネントレベルのテスト環境としてよく利用しており、その後の実装やブログでの発信に役立てています。<br />メインPCはWindows、サブとしてMacを所有しています。
        </p>
        <ul class="examples">
          <li v-for="example in env.examples" :key="example.title">
            <a v-bind:href="example.path" target="_blank"
              ><span>{{ example.title }}</span></a
            >
          </li>
        </ul>
        <ul class="keywords">
          <li v-for="keyword in env.keywords" :key="keyword">
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
      markup: {
        examples: [
          {
            title: "WEBサイト「Charlotte is Mine – official website」",
            path: "https://myscreate.com/gallery/websites-3/",
          },
          {
            title: "CodePen - profile",
            path: "https://codepen.io/mycreatesite/",
          },
        ],
        keywords: [
          "HTML5",
          "CSS3",
          "Sass(SCSS)",
          "Pug",
          "アニメーション",
          "SVGアニメーション",
        ],
      },
      js: {
        examples: [
          { title: "ポートフォリオ本サイト", path: "https://myscreate.com/" },
          {
            title: "jQueryプラグイン「TextyleFLIP.js」",
            path: "https://codepen.io/mycreatesite/pen/OrZVem",
          },
          {
            title: "Vue.js SPA（ポートフォリオサブサイト）",
            path:
              "https://myscreate.com/wp-content/themes/mycreate/pages/wicd/#/",
          },
        ],
        keywords: [
          "Javascript",
          "jQuery",
          "Vue.js",
          "Vue CLI",
          "プラグイン制作",
          "UIインタラクション",
          "SVGアニメーション",
        ],
      },
      php: {
        examples: [
          { title: "ポートフォリオ本サイト", path: "https://myscreate.com/" },
          {
            title: "WEBサイト「Charlotte is Mine – official website」",
            path: "https://myscreate.com/gallery/websites-3/",
          },
          {
            title: "WEBサイト「Kii Point Inc.」",
            path: "https://myscreate.com/gallery/websites-2/",
          },
        ],
        keywords: ["WordPress", "PHP", "XAMPP", "独自テーマ"],
      },
      env: {
        examples: [
          { title: "GitHub", path: "https://github.com/mycreatesite" },
          {
            title: "CodePen - profile",
            path: "https://codepen.io/mycreatesite/",
          },
        ],
        keywords: [
          "Windows",
          "Mac",
          "Node.js",
          "Gulp",
          "Vue CLI",
          "Git",
          "GitHub",
        ],
      },
    };
  },
};
</script>
<style scoped lang="scss">
@import "../assets/scss/common.scss";
</style>