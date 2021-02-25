<template>
    <div class="recommend">
       <div v-for="(item,index) in recommends" :key="index" class="recommend-item">
           <a :href="item.link">
               <img :src="item.image" alt="">
               <div>{{item.title}}</div>
           </a>
       </div>
    </div>
</template>
<script>

export default {
    name:"HomeRecommendView",
    props: {
        recommends: {
            type: Array,
            default(){
                return []
            }
        }
    },
      
}
</script>
<style scoped>
.recommend{
    display:flex;
    width:100%;
    align-items: center;
    text-align: center;
    justify-content:space-around;
    padding: 10px 0 15px;
    border-bottom: 8px solid #eee;
}
.recommend-item{
    flex:1;
}
.recommend-item a img{
    width: 65px;
    height: 65px;
}
</style>