<template>
  <div class="container">
    <div class="main">
      <div class="texts">
        <h1>
          <span
            v-for="(t, index) in title"
            :key="index"
            class="item"
            :style="{ animationDelay: index * 80 + 'ms' }"
            v-text="t"
          />
        </h1>
        <p style="white-space:pre-wrap; word-wrap:break-word;">
          {{ description }}
        </p>
      </div>
      <img class="mv" src="../assets/img/MV.png" alt="MV" />
    </div>
  </div>
</template>

<script>
export default {
  name: "top",
  data() {
    return {
      title: "WHAT I CAN DO.",
      description: `My name is Masayoshi Kawashima,\nas known as ma-ya's CREATE.\nThis site has created by SPA of Vue.js.`,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h1 {
  font-weight: 900;
  font-size: 13.5vh;
  color: black;
  letter-spacing: 0.4vw;
  margin: 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
p {
  text-align: left;
  font-size: 0.8rem;
  letter-spacing: 1.5px;
  line-height: 1.5;
}
.item {
  display: inline-block;
  min-width: 0.3em;
  animation: text-in 0.2s ease-out 0s backwards;
  &:nth-last-child(2),
  &:nth-last-child(3) {
    color: #4bc9c7;
  }
}
.container {
  width: 80vw;
  margin: 0 auto;
  .main {
    width: 100%;
    display: flex;
    justify-content: center;
  }
  .texts {
    position: relative;
    z-index: 1;
    padding-top: 32vh;
  }
  .mv {
    position: fixed;
    z-index: -1;
    bottom: 0;
    left: 50%;
    transform: translate(-50%, 0) scale(1);
    display: block;
    width: auto;
    height: 79vh;
    animation: mv-fade 1.2s cubic-bezier(0.86, 0, 0.07, 1) 1s backwards;
  }
}
@keyframes mv-fade {
  0% {
    opacity: 0;
    transform: translate(-35%, 10%) scale(1.5);
  }
}
@keyframes text-in {
  0% {
    transform: translate(-5px, 5px);
    opacity: 0;
  }
}
@media screen and (max-width: 900px) {
  p {
    text-align: center;
  }
  h1 {
    font-size: 11.5vw;
    letter-spacing: 2px;
  }
  .container {
    width: 100%;
    .texts {
      padding-top: 5vh;
    }
    .mv {
      height: 60vh;
    }
  }
}
@media screen and (max-width: 420px) {
  h1 {
    font-size: 11vw;
    letter-spacing: 1px;
  }
  p {
    font-size: 0.7rem;
  }
  .container {
    .mv {
      height: 50vh;
    }
    .texts {
      padding-top: 8vh;
    }
  }
}
</style>