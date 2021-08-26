<template>
  <div class="">
    <button @click="getNumber">点我取值</button>
  </div>
</template>

<script>
const mixin = {
  data() {
    return {
      numValue: 666
    }
  },
  methods: {
    getNumber() {
      console.log('值：', this.numValue)
    }
  }
}
export default {
  mixins: [mixin],
  data() {
    return {
    }
  }
}
</script>
<style lang="scss" scoped>
</style>