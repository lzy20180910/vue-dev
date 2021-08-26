<template>
  <div class="">
    <button @click="open">开</button>
    <button @click="close">关</button>
  </div>
</template>

<script>
export default {
  prop: ['show'],
  data() {
    return {
    }
  },
  methods: {
    open() {
      this.$emit('update:show', true)
    },
    close() {
      this.$emit('update:show', false)
    }
  }
}
</script>
<style lang="scss" scoped>
</style>