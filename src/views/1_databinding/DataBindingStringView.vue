<template>
<div>
    <h1>Hello {{ userName }}</h1>
    <p>
        {{ message }}
    </p>
</div>

</template>
<!-- 뷰에서 html 태그의 경우 최상위 태그가 있고,
그 다음에 같은 레벨의 태그들을 여러 개 사용해야 에러(빨간 줄)가 안난다
예를 들어 h1 태그, p태그를 같이 사용했을 때, div 태그가 없는 경우 에러가 남
 -->
<script>
export default {
  data() {
    return {
      userName: 'John',
      message: 'Welcome man'

    }
  }
}
</script>

<style scoped>
.text-red{
    color: red;
}
</style>

<!-- scoped는 이 현재 작성된 곳에만 사용 가능 이 화면에만 적용해야 할 것을 작성
scoped를 빼면 모든 컴포넌트에서 <text-red>라는 것을 사용 가능 -->
