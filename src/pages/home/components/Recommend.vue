<template>
<div class="">
    <div class="recommend-title">
        热销推荐
    </div>
    <ul>
        <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
            <div class="item-img-wrapper">
                <img class="item-img" :src="item.imgUrl">
            </div>
            <div class="item-info">
                <p class="item-title">{{item.title}}</p>
                <p class="item-desc">{{item.desc}}</p>
                <button class="item-button">查看详情</button>
            </div>
        </li>
    </ul>
</div>
</template>

<script>
export default {
    name:'HomeRecommend',
    data(){
        return{
            recommendList:[{
                id:'0001',
                imgUrl:'http://img1.qunarzz.com/sight/p0/1508/12/4e6170303c63bdb7070fb1987480afab.water.jpg_200x200_0775a71c.jpg',
                title:'杭州极地海洋世界',
                desc:'你的司机那次 i 啊纠结反复'
            },{
                id:'0002',
                imgUrl:'http://img1.qunarzz.com/sight/p0/1508/12/4e6170303c63bdb7070fb1987480afab.water.jpg_200x200_0775a71c.jpg',
                title:'杭州极地海洋世界',
                desc:'你的司机那次 i 啊纠结反复'
            },{
                id:'0003',
                imgUrl:'http://img1.qunarzz.com/sight/p0/1508/12/4e6170303c63bdb7070fb1987480afab.water.jpg_200x200_0775a71c.jpg',
                title:'杭州极地海洋世界',
                desc:'你的司机那次 i 啊纠结反复'
            },{
                id:'0004',
                imgUrl:'http://img1.qunarzz.com/sight/p0/1508/12/4e6170303c63bdb7070fb1987480afab.water.jpg_200x200_0775a71c.jpg',
                title:'杭州极地海洋世界',
                desc:'你的司机那次 i 啊纠结反复'
            }]
        }
    }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl';

.recommend-title
    margin-top:.2rem
    line-height:.8rem
    background #eee
    text-indent:.2rem
.item
    display:flex
    overflow:hidden
    height:1.9rem
    .item-img
        width:1.7rem
        height:1.7rem
        padding:.1rem
    .item-info
        flex:1
        padding:.1rem
        min-width:0
        .item-title
            line-height:.54rem 
            font-size:.32rem 
            ellipsis()
        .item-desc
            line-height:.4rem 
            color:#ccc
            ellipsis()
        .item-button
            line-height:.44rem
            margin-top:.16rem
            background:#ff9300
            color:#fff
            padding:0 .2rem
            border-radius:.06rem

</style>
