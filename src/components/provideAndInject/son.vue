<template>
  <div class="">
    <h2>{{exp}}</h2>
    <grandson />
  </div>
</template>

<script>
import grandson from './grandson.vue'
export default {
  inject: ['exp'],
  components: { grandson },
  data() {
    return {
    };
  },
}
</script>
<style lang="scss" scoped>
</style>