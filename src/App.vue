<!-- template: HTML, CSS 등의 마크업 속성과 뷰 인스턴스에서 정의한 데이터 및 로직들을 연결하여 사용자가 브라우저에서 볼 수 있는 형태의 HTML로 변환해주는 속성 -->
<template>
  <div class="black-bg" v-if="modal_opened == true">
    <div class="white-bg">
      <h4>상세페이지</h4>
      <p>상세페이지 내용</p>
    </div>
  </div>
  <div class="menu">
    <a v-for="a in navbar" :key="a">{{ a }}</a>
  </div>

  <div>
    <img src="./assets/room0.jpg" class="room-img"> <!-- 상대경로(현재 위치에서부터) -->
    <h4 @click="modal_opened = true"> 역삼동원룸 </h4>
    <p> 50만원</p>
    <button @click="declare_num[0]++">허위매물신고</button>
    <span> 신고수 : {{ declare_num[0] }}</span>
  </div>

  <div>
    <img src="./assets/room1.jpg" class="room-img">
    <h4> 효자동원룸 </h4>
    <p> 50만원</p>

    <button @click="declare_num[0]++">허위매물신고</button>
    <span> 신고수 : {{ declare_num[0] }}</span>
  </div>

  <div>
    <img src="./assets/room2.jpg" class="room-img">
    <h4> 마포구원룸 </h4>
    <p> 50만원</p>

    <button @click="declare_num[0]++">허위매물신고</button>
    <span> 신고수 : {{ declare_num[0] }}</span>
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
      modal_opened: false, // UI 상태 저장 -> 'state'
      declare_num: [0,0,0],
      navbar : ['Home', 'Shop', 'About'],
    }
  },
  components: {
  }
}
</script>

<style>
body {
  margin : 0;
}

div {
  box-sizing: border-box;
}
.black-bg {
  width: 100%;
  height: 100%;
  background: rgba(0,0,0,0.5);
  position: fixed;
  padding: 20px;
}
.white-bg {
  width: 100%;
  background: white;
  border-radius: 8px;
  padding: 20px;
}

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

.room-img {
  width: 80%;
  margin-top: 40px;
}

</style>
