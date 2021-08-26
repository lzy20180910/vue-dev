<template>
  <!-- 修饰符的使用 -->
  <div class="">
    <!-- 1.表单修饰符 -->
    <!-- lazy  -->
    <p>在我们填完信息，光标离开标签的时候，才会将值赋予给value，也就是在change事件之后再进行信息同步</p>
    <input type="text" v-model.lazy="text1"/>
    <p>{{text1}}</p>

    <!-- trim -->
    <p>自动过滤用户输入的首空格字符，而中间的空格不会过滤</p>
    <input type="text" v-model.trim="text2">
    <p>{{text2}}</p>

    <!-- number -->
    <p>自动将用户的输入值转为数值类型，但如果这个值无法被parseFloat解析，则会返回原来的值</p>
    <input type="text" v-model.number="text3">
    <p>{{text3}}</p>


    <!-- 2.事件修饰符，事件修饰符是对事件捕获以及目标进行了处理，有如下修饰符： -->
    <!-- stop、prevent、self、once、capture、passive、native -->
    <!-- stop -->
    <div @click="click1">
      <button @click.stop="click2">我已经阻止了事件冒泡，不信你点点</button>
    </div>

    <h1>这是新增加的</h1>

  </div>
</template>

<script>
export default {
  data() {
    return {
      text1: '',
      text2: '',
      text3: ''
    }
  },
  methods: {
    click1() {
      console.log('我是父元素事件')
    },
    click2() {
      console.log('我是子元素事件')
    }
  }
}
</script>
<style lang="scss" scoped>
</style>