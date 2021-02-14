<template>
  <header>
    <nav>
      <ul>
        <li v-for="(item, index) in items" :key=index>
            <router-link v-bind:to=item.path exact>
              {{ item.title }}
            </router-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'menuList',
  data () {
    return {
      items: [
        { title: 'TOP', path: '/' },
        { title: 'DESIGNS', path: '/designs' },
        { title: 'CORDINGS', path: '/cordings' }
      ]
    }
  }
}
</script>

<style scoped>
header {
  width : 80vw;
  margin : 0 auto;
  padding-top : 100px;
}
ul {
  list-style-type: none;
  margin : 0;
  padding : 0;
  font-size : 18px;
  font-weight : 900;
  letter-spacing: 2px;
  text-align: center;
}
li {
  display : inline-block;
  padding : 0 1rem;
}
a {
  display : block;
  position : relative;
  text-decoration: none;
  color : #000;
  padding : 0 1rem;
  line-height: 1.5;
}
a::before {
  content: '';
  display : block;
  position : absolute;
  z-index : -1;
  top : 0;
  left : 0;
  width : 0;
  height : 100%;
  opacity : 0;
  background : #A9E8E8;
  transition : all .3s ease-in-out;
}
a.router-link-active::before {
  width : 100%;
  opacity : 1;
}
@media screen and (max-width:900px) {
  header {
    width : 100%;
  }
  li {
    padding : 0 2vw;
  }
  a {
    padding : 0 2vw;
  }
}
@media screen and (max-width:420px) {
  header {
    padding-top : 12vh;
    width : 100%;
  }
  ul {
    font-size : 1rem;
  }
}
</style>