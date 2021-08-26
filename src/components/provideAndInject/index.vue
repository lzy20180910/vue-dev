<template>
  <div class="">
    <son />
  </div>
</template>

<script>
import son from './son.vue'
export default {
  components: { son },
  provide:{
    exp: '注入的exp值'
  },
  data() {
    return {
    };
  },
}
</script>
<style lang="scss" scoped>
</style>