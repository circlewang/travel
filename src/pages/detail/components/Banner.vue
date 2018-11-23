<template>
<div>
    <div class="banner" @click="handleBannerClick">
        <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1411/b6/662fc49d1d26a5a7775cf6b7f8b4ecec.water.jpg_600x330_c34588e7.jpg">
        <div class="banner-info">
            <div class="banner-title">印象西湖</div>
            <div class="banner-number">
                <span class="iconfont banner-icon">&#xe692;</span>
                39
            </div>
        </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
</div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
    name:'DetailBanner',
    components:{
        CommonGallary
    },
    data(){
        return{
            showGallary:false,
            imgs:['http://img1.qunarzz.com/sight/p0/1411/c0/510cdcb852590824eb40027bb011c18a.water.jpg_r_800x800_5e94080e.jpg','http://img1.qunarzz.com/sight/p0/1505/4f/4f078c2959fb4b05.water.jpg_r_800x800_c1f01394.jpg']
        }
    },
    methods:{
        handleBannerClick(){
            this.showGallary=true;
        },
        handleGallaryClose(){
            this.showGallary=false;
        }
    }
}
</script>

<style lang="stylus" scoped>
    .banner
        position:relative
        overflow:hidden
        width:100%
        height:0
        padding-bottom:55%
        .banner-img 
            width:100%;
        .banner-info
            display:flex
            position:absolute
            left:0
            right:0
            bottom:0
            line-height:.6rem
            color:#fff
            background-image:linear-gradient(top,rgba(0,0,0,0),rgba(0,0,0,0.8))
            .banner-title
                flex:1
                font-size:.32rem
                padding:0 .2rem
            .banner-number
                padding:0 .4rem
                line-height:.32rem 
                height:.32rem 
                border-radius:.2rem 
                background:rgba(0,0,0,0.8)
                font-size:.24rem
                margin-top:.14rem
                .banner-icon
                    font-size:.24rem

</style>