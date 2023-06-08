<template>
  <li>{{ name }}</li>

</template>


<script>
export default {
  props: {
    name: {
      type: String,
      default: ''
    }
  }
}
</script>

<style scoped lang="scss"> //scoped는 현재페이지에서만 스타일이 적용되게끔 유효범위를 설정함
h1{
  color: red !important;
}
</style>