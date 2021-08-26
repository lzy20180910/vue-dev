<template>
  <div class="">
    <h3>孙子组件：{{exp}}</h3>
  </div>
</template>

<script>
export default {
  inject: ['exp'],
  data() {
    return {
    };
  },
}
</script>
<style lang="scss" scoped>
</style>