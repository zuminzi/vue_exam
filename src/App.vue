<!-- template: HTML, CSS 등의 마크업 속성과 뷰 인스턴스에서 정의한 데이터 및 로직들을 연결하여 사용자가 브라우저에서 볼 수 있는 형태의 HTML로 변환해주는 속성 -->
<template>
  <div class="menu">
    <a v-for="a in navbar" :key="a">{{ a }}</a>
  </div>

  <img alt="Vue logo" src="./assets/logo.png">
  <div v-for="(n,i) in products" :key="n">
    <h4> {{ products[i].name }} </h4>
    <p> {{ products[i].price }} 만원</p> <!--{{데이터바인딩 문법}} -->
  </div>
</template>

<script>
export default {
  name: 'App',

  data(){
    return {
      // 데이터바인딩을 위한 데이터 보관함
      // 데이터바인딩이란? JS데이터(뷰 인스턴스의 데이터)와 HTML 요소 바인딩
      // 데이터바인딩 장점? 실시간 자동 렌더링
      navbar : ['Home', 'Shop', 'About'],
      products : [{name: '역삼동원룸', price: 50}, {name: '천호동원룸', price: 60}, {name: '마포구원룸', price: 70}]
    }
  },
  components: {
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}

.menu a {
  color: white;
  padding: 10px;
}

</style>
