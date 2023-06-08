<template>
  <h1 @click="increase
  ">{{ count }}
  </h1>
  <div v-if="count > 4">
    4보다 큽니다!
  </div>
  <ul>
    <hellow 
    v-for="fruit in fruits" 
    :key="fruit" 
    :name="fruit">
    {{ fruit }}
    </hellow>
  </ul>
</template>

<script>
import Fruit from '~/components/Fruit'
export default{
  components:{
    hellow: Fruit
  },
  data(){
    return {
      count: 0,
      fruits: ['apple', 'banana', 'cherry']
    }
  },
  methods: {//메소드 > 이벤트 핸들러 /반응성 (데이터를 갱신하면 화면이 바뀐다.)
    increase(){
      this.count += 1
    }
  }
}
</script>

<style lang="scss">
h1{
  font-size: 50px;
  color: royalblue;
}
ul{
  li{
    font-size: 40px;
  }
}
</style>