<template>
  <div class="">
    <h2>$attrs和$listeners的使用</h2>
    <child aprop="aprpp-value" :age="18" sex="男" @sendMsg="getMsg"></child>
  </div>
</template>

<script>
import child from './child.vue'
export default {
  components: { child },
  data() {
    return {
    };
  },
  methods: {
    getMsg(msg) {
      console.log('msg:',msg)
    }
  }
}
</script>
<style lang="scss" scoped>
</style>