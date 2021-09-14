<template>
  <div class="myui-block">
    <slot></slot>
  </div>
</template>
<script>
export default {
  name: 'MyBlock',
  data() {
    return {
      direction: '90deg'
    }
  },
  mounted() {
  }
}
</script>
<style scoped lang="scss">
@mixin text-default {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.myui-block {
  @include text-default;
  border: solid lightgray 1px {
    radius: 5px;
  }
  margin: 2px;
  padding: 10px;
  background: aliceblue;
}
</style>