<template>
  <div>
    <div id="butt">
      <img src="~/static/tup.jpg" class="ppp" />
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
      a: '弹窗',
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
  background: red;
}
#butt {
  margin-top: 10%;
  display: flex;
  justify-content: center;
}
#buttt {
  margin-top: 30%;
  display: flex;
  justify-content: center;
  background: yellow;
}
.ppp {
  width: 50px;
  height: 50px;
}
</style>