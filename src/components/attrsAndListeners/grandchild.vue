<template>
  <div class="">
    <h4 @click="clickMe">{{sex}}</h4>
    <h4>{{aprop}}</h4>
  </div>
</template>

<script>
export default {
  props: ['sex', 'aprop'],
  data() {
    return {
    };
  },
  methods: {
    clickMe() {
      this.$emit('sendMsg', '这是孙子组件传来的信息')
    }
  }
}
</script>
<style lang="scss" scoped>
</style>