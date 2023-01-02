<!-- template: HTML, CSS 등의 마크업 속성과 뷰 인스턴스에서 정의한 데이터 및 로직들을 연결하여 사용자가 브라우저에서 볼 수 있는 형태의 HTML로 변환해주는 속성 -->
<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div>
    Vuedongsan <!--실시간으로 변경될 일이 없는 데이터는 굳이 데이터바인딩 X -->
    <h4> xx 원룸 </h4>
    <p> {{ price1 }} 만원</p> <!--{{데이터바인딩 문법}} -->
  </div>
  <div>
    <h4> xx 원룸 </h4>
    <p> {{ price2 }} 만원</p>
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
      price1 : 60,
      price2 : 70,
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
</style>
