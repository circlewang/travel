<template>
<div>
    <div class="title">
       周末去哪儿
    </div>
    <ul>
        <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
            <div class="item-img-wrapper">
                <img class="item-img" :src="item.imgUrl">
            </div>
            <div class="item-info">
                <p class="item-title">{{item.title}}</p>
                <p class="item-desc">{{item.desc}}</p>
            </div>
        </li>
    </ul>
</div>
</template>

<script>
export default {
    name:'HomeWeekend',
    data(){
        return{
            recommendList:[{
                id:'0001',
                imgUrl:'http://img1.qunarzz.com/sight/source/1510/c1/afe3ab32b3bc23.jpg_r_640x214_beb61760.jpg',
                title:'杭州极地海洋世界',
                desc:'你的司机那次 i 啊纠结反复'
            },{
                id:'0002',
                imgUrl:'http://img1.qunarzz.com/sight/source/1510/c1/afe3ab32b3bc23.jpg_r_640x214_beb61760.jpg',
                title:'杭州极地海洋世界',
                desc:'你的司机那次 i 啊纠结反复'
            },{
                id:'0003',
                imgUrl:'http://img1.qunarzz.com/sight/source/1510/c1/afe3ab32b3bc23.jpg_r_640x214_beb61760.jpg',
                title:'杭州极地海洋世界',
                desc:'你的司机那次 i 啊纠结反复'
            }]
        }
    }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl';

    .title
        line-height:.8rem
        background #eee
        text-indent:.2rem
    .item-img-wrapper
        overflow:hidden
        height:0
        padding-bottom:33.9%
        .item-img
            width:100%
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
       

</style>
