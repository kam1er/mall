<template>
  <!-- ref 绑定到组件上面 -->
  <div ref="wrapper" class="wrapper">
    <div>
      <slot></slot>
    </div>
  </div>
</template>
<script>
import BScroll from "better-scroll";
export default {
  name: "Scroller",
  props: {
    probeType:{
      type: Number,
      default:0
    },
    pullUpLoad:{
      type:Boolean,
      default:false
    }
  },
  data() {
    return {
      scroller: null
    };
  },
  mounted() {
    // 1.创建BScroll对象
    this.scroller = new BScroll(document.querySelector(".wrapper"), {
      probeType: this.probeType,
      pullUpLoad: this.pullUpLoad,
      click: true
    });
    // 2.监听滚动的位置
    this.scroller.on('scroll',(position) =>{
      this.$emit("scroll",position)
    })
    // 3.监听上拉界面
    this.scroller.on('pullingUp',()=>{
     this.$emit("pullingUp")
    })
  },
  methods: {
    scrollTo(x, y, time) {
      this.scroller.scrollTo(x,y,time)
    }
  }
};
</script>
<style scoped></style>
