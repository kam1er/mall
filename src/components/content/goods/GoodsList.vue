<template>
  <div class="good-list">
    <goods-list-item
      :goodsItem="item"
      v-for="(item, index) in goods"
      :key="index"
    />
  </div>
</template>
<script>
import GoodsListItem from "./GoodsListItem";
export default {
  name: "GoodsList",
  components: {
    GoodsListItem
  },
  props: {
    goods: {
      type: Array,
      default() {
        return [];
      }
    }
  }
};
</script>
<style scoped>
.good-list {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  background-color: var(--color-background);
  padding: 2px;
}
</style>
