<template>
  <img alt="Vue logo" src="./assets/studybugs.png" style="width:25%;">
<!--  <HelloWorld msg="Welcome to Your Vue.js App"/>-->
  <p>
  즐겁고 행복한 하루가 {{ nickname }} 님을 기다려요!
  </p>

  <span> 12 * until next Reward {{ star_count }} / 12* </span>
  <p onclick="alert('공지')"> What's New </p>
  <ul>
    <li v-for="item in noticeList" v-bind:key="item">
      {{ item.value }}
    </li>
  </ul>

  {{ nickname }} 님을 위한 추천 메뉴
  <ul>
    <li v-for="item in recommended_items" v-bind:key="item">
      {{ item.value }}
    </li>
  </ul>
  <p>
    <!-- 네비게이션을 위해 router-link 컴포넌트를 사용합니다. -->
    <!-- 구체적인 속성은 `to` prop을 이용합니다. -->
    <!-- 기본적으로 `<router-link>`는 `<a>` 태그로 렌더링됩니다.-->
    <router-link to="/Menu">Go to Menu</router-link>
  </p>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
  },

  data() {
      return {
        noticeList: [{value:'공지1'}, {value:'공지2'}],
        nickname: "린예",
        star_count: 5,
        recommended_items: [{value:'아이스 유자 민트 티'}, {value:'더블 에스프레소 칩 프라푸치노'}],
      }
  },

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
