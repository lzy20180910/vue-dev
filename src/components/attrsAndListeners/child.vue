<template>
  <div class="">
    <h3>{{age}}</h3>
    <h3>{{$attrs}}</h3>
    <grandchild v-bind="$attrs" v-on="$listeners"></grandchild>
  </div>
</template>

<script>
import grandchild from './grandchild.vue'
export default {
  components: { grandchild },
  props: ['age'],
  data() {
    return {
    };
  },
}
</script>
<style lang="scss" scoped>
</style>