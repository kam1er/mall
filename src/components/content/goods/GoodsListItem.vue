<template>
  <div class="goods">
      <img :src="goodsItem.show.img" alt="">
      <div>
          <p>{{goodsItem.title}}</p>
          <span class="price">{{goodsItem.price}}</span>
          <span class="collect">{{goodsItem.cfav}}</span>
      </div>
  </div>
</template>
<script>
export default {
  name: "GoodsListItem",
  props: {
    goodsItem: {
      type: Object,
      default() {
        return [];
      }
    }
  }
};
</script>
<style scoped>
.goods{
    width: 100%;
    display: flex;
}
.goods img{
    width: 200px;
    padding: 5px;
}
</style>
