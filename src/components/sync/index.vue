<template>
  <div class="">
    <h2>sync修饰符的使用</h2>
    <sync :show.sync="isShow"/>
    <div v-show="isShow">检测isShow是否有同步变化{{isShow}}</div>
    <sync :show.sync="isShow2"/>
    <div v-show="isShow2">检测isShow和isShow2会不会冲突</div>
  </div>
</template>

<script>
import sync from './sync.vue'
export default {
  components: { sync },
  data() {
    return {
      isShow: false,
      isShow2: false
    };
  },
}
</script>
<style lang="scss" scoped>
</style>