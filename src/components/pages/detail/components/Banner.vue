<template>
    <div>    
        <div class="banner" @click="handleBannerClick" >
            <img class="banner-img" src="//img1.qunarzz.com/sight/p0/201301/08/6f52991818c4b8ea93835fbb.jpg_600x330_2d24cc3f.jpg" alt="">
            <div class="banner-info">
                <div class="banner-title" >天台山琼台仙谷</div>
                <div class="banner-number" >
                    <span class="iconfont banner-icon">&#xe692;</span>7
                </div>
            </div>
        </div>
        <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose" ></common-gallary>
    </div>
    
</template>

<script>
    import CommonGallary from 'common/gallary/Gallary.vue'
    export default {
        name: "DetailBanner",
        data(){
            return {
                showGallary:false,
                imgs:['http://img1.qunarzz.com/sight/p0/1412/66/cd09ac9548221dcc4cef8dde5913c780.water.jpg_r_800x800_bea4d4a4.jpg','http://img1.qunarzz.com/sight/p0/201301/08/6f52991818c4b8ea93835fbb.jpg_600x330_2d24cc3f.jpg']
            }
        },
        methods:{
            handleBannerClick(){
                this.showGallary = true;
            },
            handleGallaryClose(){
                this.showGallary = false
            }
        },
        components:{
            CommonGallary,
        }
    }
</script>

<style lang="stylus"  scoped>
    .banner
        position:relative
        overflow:hidden
        height:0
        padding-bottom:55%
        .banner-img
            width:100%
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
                flex: 1
                font-size: .32rem
                padding: 0 .2rem
            .banner-number 
                margin-top:.14rem
                padding: 0 .4rem
                height: .32rem
                line-height: .32rem
                border-radius: .2rem
                background: rgba(0,0,0,.8)
                font-size: .24rem
                .banner-icon
                    font-size: .24rem
                


    
</style>