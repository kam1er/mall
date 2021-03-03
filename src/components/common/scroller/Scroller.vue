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
  data() {
    return {
      scroller: null
    };
  },
  mounted() {
    this.scroller = new BScroll(document.querySelector('.wrapper'), {
       probeType: 2,
       click:true
    });
    //  console.log( this.scroller)
    this.scroller.on('scroll',(position)=>{
      console.log(position)
    })
  }
};
</script>
<style scoped>

</style>
