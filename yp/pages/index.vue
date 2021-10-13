<template>
  <div>
    <div>
      <img src="~/static/tup.jpg" class="ppp" />

      <div class="left-1">
        <div>信息</div>
        <div>通讯录</div>
      </div>
    </div>
    <div id="buttt">
      <button class="but" @click="bindXXX">{{ a }}</button>
    </div>
  </div>
</template>
<script>
import Vue from 'vue'
export default Vue.extend({
  data() {
    return {
      a: '登录',
    }
  },
  head: {
    script: [
      {
        src: 'https://cdn.bootcdn.net/ajax/libs/limonte-sweetalert2/11.1.0/sweetalert2.all.js',
      },
      {
        src: '~/assets/css.p/tupian.jpg',
      },
    ],
  },
  created() {}, // 渲染前 虚拟dom
  mounted() {}, // 渲染后 window 有dom
  // updated() {}, // 不用
  // destroyed() {},
  methods: {
    bindXXX() {
      Swal.fire({
        title: '<strong>示例 <u>aaa</u></strong>',
        icon: 'info',
        html:
          'You can use <b>bold text</b>, ' +
          // '<a href="//sweetalert2.github.io">links</a> ' +
          'and other HTML tags',
        showCloseButton: true,
        showCancelButton: true,
        focusConfirm: false,
        confirmButtonText: '<i class="fa fa-thumbs-up"></i> 好',
        confirmButtonAriaLabel: 'Thumbs up, great!',
        cancelButtonText: '<i class="fa fa-thumbs-down">差</i>',
        cancelButtonAriaLabel: 'Thumbs down',
      }).then((result) => {
        console.log('🌊', result)
      })
    },
  },
})
</script>
<style>
.but {
  width: 50px;
  height: 50px;
  margin-top: 25px;
  background: red;
}

#buttt {
  height: 100px;
  left: 160px;
  right: 0%;
  display: flex;
  justify-content: center;
  background: yellow;
  position: absolute;
  top: 630px;
}
.ppp {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  position: absolute;
  left: 50%;
  top: 100px;
}
.left-1 {
  background: rgb(99, 97, 97);
  width: 150px;
  height: 100vh;
}
</style>