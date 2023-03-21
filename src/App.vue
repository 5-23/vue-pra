<template>
  {{ hello() }}

  var: <b v-on:click="asdf++ /* 클릭 이벤트 */"> {{ asdf /* 변수사용 */ }} </b> <br/>
  <!-- @click에서 @는 `v-on:`를 생략한거 -->
  var: <b @click="asdf++ /* 클릭 이벤트 */"> {{ asdf /* 변수사용 */ }} </b>

  <!-- v-if: 안에 있는 조건이 true일때만 테그를 보여줌 -->
  <h1 v-if="asdf %2 == 0">짝수임!</h1>

  <!-- 반복문 -->
  <a v-for="i in 10" :key="i" :href="`#${i}`">
    <br>
    {{ i-1 }}번째 div
  </a>


</template>

<script>

export default {
  name: "App",
  data(){
    return {
      asdf: 10 // 이렇게 변수 저장함
    }
  },
  methods:{
    hello(){
      console.log(`hello! ${this.asdf /* 변수 사용 */}`) // 함수
    }
  },
  components: {

  }
}
</script>