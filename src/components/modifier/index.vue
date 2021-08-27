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

    <!-- once -->
    <p>自动将用户的输入值转为数值类型，但如果这个值无法被parseFloat解析，则会返回原来的值</p>
    <div>
      <button @click.once="click2">我的点击事件只会执行一次</button>
    </div>


    <!-- 3.鼠标按钮修饰符，鼠标按钮修饰符针对的就是左键、右键、中键点击，有如下： -->
    <!-- left 、right、middle -->
    <!-- left -->
    <button @click.left="click2">鼠标左键点击</button>
    <!-- right -->
    <button @contextmenu.prevent="click2" >鼠标右键点击</button>
    <!-- middle -->
    <button @click.middle="click2">鼠标中键点击</button>

    
    <!-- 3.键盘修饰符，键盘修饰符是用来修饰键盘事件（onkeyup，onkeydown）的，有如下： -->
    <!-- keyCode存在很多，但vue为我们提供了别名，分为以下两种：
    普通键（enter、tab、delete、space、esc、up...）
    系统修饰键（ctrl、alt、meta、shift...） -->
    <input type="text" @keyup.enter="asd" />

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
    },
    asd() {
      console.log('按了回车键了')
    }
  }
}
</script>
<style lang="scss" scoped>
</style>