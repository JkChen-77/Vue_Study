<template>
  <div
    :class="clsname"
    :style="{
      top: top,
      background:msgBgColor,
      borderRadius: borderRadius
    }"
  >
    <h3
      :style="{
        color:titleColor,
        fontsize:titleSize,
        background:titleBgColor,
        borderTopLeftRadius: borderRadius,
        borderTopRightRadius: borderRadius
      }"
    >
      {{ title }}
    </h3>
    <div
      class="content"
      :style="{
        color:msgColor,
        fontsize:msgSize
      }"
    >
      {{ messages }}
    </div>
      <div class="btn">
        <slot />
      </div>
  </div>
</template>

<script>

export default {
  name: 'Popup',
  props: {
    title: {
      type: String,
      default: '提示'
    },
    messages: {
      type: String,
      default: '你好！'
    },
    borderRadius: {
      type: String,
      default: '15px'
    },
    top: {
      type: String,
      default: '100px'
    },
    titleColor: {
      type: String,
      default: 'rgb(243, 241, 129)'
    },
    titleSize: {
      type: String,
      default: '14px'
    },
    titleBgColor: {
      type: String,
      default: 'rgb(134, 95, 206)'
    },
    msgColor: {
      type: String,
      default: '#666'
    },
    msgSize: {
      type: String,
      default: '14px'
    },
    msgBgColor: {
      type: String,
      default: 'rgba(200,200,200,0.5)'
    },
    movies: {
      type: String,
      default: 'zoomInDown'
    }
  },
  data() {
    return {
      clsname: ''
    }
  },
  mounted() {
    this.clsname = `container animate__animated animate__animated animate__${this.movies}`
  }
}
</script>

<style scoped lang="scss">
.container {
  padding: 0;
  position: fixed;
  left: 50%;
  transform: translate(-50%, 0);
  width: 500px;
  height: 300px;
    h3{
        margin: 0;
        height: 10%;
        background: rgb(243, 241, 129);
        padding-left: 20px;
    }
  .content {
    text-align: center;
    height: 180px;
  }
  .btn{
      width: 70px;
      margin: 0 auto;
  }
}
</style>
