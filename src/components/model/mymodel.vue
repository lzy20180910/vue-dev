<template>
  <div class="">
    <button @click="add">点我加1</button>
  </div>
</template>

<script>
export default {
  props: ['counts'],
  model: {
    props: 'counts',
    event: 'changes'
  },
  data() {
    return {
      num: 0
    };
  },
  methods: {
    add() {
      this.$emit('changes', ++this.num)
    }
  }
}
</script>
<style lang="scss" scoped>
</style>