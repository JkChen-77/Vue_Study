<template>
  <div class="message">
    <h1>全局动画弹窗</h1>
    <el-button @click="open('bounce')">bounce</el-button>
    <el-button @click="open('flash')">flash</el-button>
    <el-button @click="open('pulse')">pulse</el-button>
    <el-button @click="open('rubberBand')">rubberBand</el-button>
    <el-button @click="open('shakeX')">shakeX</el-button>
    <el-button @click="open('shakeY')">shakeY</el-button>
    <el-button @click="open('headShake')">headShake</el-button>
    <el-button @click="open('tada')">tada</el-button>
    <el-button @click="open('wobble')">wobble</el-button>
    <el-button @click="open('jello')">jello</el-button>
    <el-button @click="open('heartBeat')">heartBeat</el-button>
    <el-button @click="open('backInDown')">backInDown</el-button>
    <el-button @click="open('backInLeft')">backInLeft</el-button>
    <el-button @click="open('backInRight')">backInRight</el-button>
    <el-button @click="open('backOutDown')">backOutDown</el-button>
    <el-button @click="open('backOutLeft')">backOutLeft</el-button>
    <el-button @click="open('backOutRight')">backOutRight</el-button>
    <el-button @click="open('backOutUp')">backOutUp</el-button>
  </div>
</template>

<script>
export default {
  name: 'Dashboard',
  mounted() {
  },
  methods: {
    open(movies) {
      this.$Box({
        title: '警告！',
        messages: '晚上好！',
        msgBgColor: 'rgba(200,200,200,0.5)',
        top: '50px',
        movies: movies
      }, {
        btn: <el-button type='success'>确认</el-button>
      }).init()
    }
  }
}
</script>

<style scoped>

</style>
