<template>
  <div class="">
    <h2>父组件的count:{{count}}</h2>
    <mymodel v-model="count" />
  </div>
</template>

<script>
import mymodel from './mymodel.vue'
export default {
  components: {mymodel},
  data() {
    return {
      count: 0
    };
  },
}
</script>
<style lang="scss" scoped>
</style>