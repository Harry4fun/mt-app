<template>
    <section class="m-istyle">
        <dl @mouseover="over">
            <dt>有格调</dt>
            <dd
                :class="{active:kind==='all'}"
                kind="all"
                keyword="景点" >全部</dd>
            <dd
                :class="{active:kind==='part'}"
                kind="part"
                keyword="美食">约会聚餐</dd>
            <dd
                :class="{active:kind==='spa'}"
                kind="spa"
                keyword="丽人">丽人SPA</dd>
            <dd
                :class="{active:kind==='movie'}"
                kind="movie"
                keyword="电影">电影演出</dd>
            <dd :class="{active:kind === 'travel'}"
                kind="travel"
                keyword="旅游">品质出游</dd>                    
        </dl>
        <ul class="ibody">
            <li v-for="(item,idx) in cur" :key="idx" >
                <el-card :body-style="{ padding: '0px' }"
                    shadow="never">
                    <img :src="item.img" class="image">
                    <ul>
                        <li class="title">{{item.title}}</li>
                        <li class="pos">{{item.pos}}</li>
                        <li class="price">￥<em>{{ item.price }}</em><span>/起</span></li>
                    </ul>
                </el-card>
            </li>
        </ul>
    </section>
</template>
<style lang="scss">
    @import "@/assets/css/index/artistic.scss";
</style>
<script>
    export default{
        data() {
            return {
                kind:'all',
                list:{
                    all: [{
                        img:'http://p1.meituan.net/msmerchant/3fb7c5ebb2e57003dc4a0733568c9683339216.jpg@368w_208h_1e_1c',
                        title:'百年义利（垡头店）',
                        pos:'清河',
                        price:200
                    },{
                        img:'http://p0.meituan.net/mogu/fc091566222b23c51857ab4316633e43370925.jpg@368w_208h_1e_1c',
                        title:'祈年八号中餐厅',
                        pos:'崇文门新世界',
                        price:98
                    },{
                        img:'http://p0.meituan.net/msmerchant/1a8aaac8cfcf76fae83c2ecd6405bd4c1457315.jpg@368w_208h_1e_1c',
                        title:'北京饭店阳光咖啡厅',
                        pos:'王府井/东单',
                        price:238
                    },{
                        img:'https://img.meituan.net/msmerchant/3fb7c5ebb2e57003dc4a0733568c9683339216.jpg@380w_214h_1e_1c',
                        title:'金掌勺东北菜（王府井店）',
                        pos:'王府井/东单',
                        price:69
                    },{
                        img:'http://p1.meituan.net/wedding/8d26f93de654d433b17774e60a1fc5bd1028431.jpg@240w_180h_1e_1c_1l|watermark=1&&r=2&p=9&x=2&y=2&relative=1&o=20|368w_208h_1e_1c',
                        title:'木北造型（崇文门新世界店)',
                        pos:'崇文门新世界',
                        price:421
                    },{
                        img:'http://p1.meituan.net/dpmerchantalbum/df6753726f5fe30a19139166c7fbe704119922.jpeg@368w_208h_1e_1c',
                        title:'江南赋（内蒙古大厦店）',
                        pos:'王府井/东单',
                        price:114
                    }
                    ],
                    part: [{
                        img:'http://p1.meituan.net/msmerchant/3fb7c5ebb2e57003dc4a0733568c9683339216.jpg@368w_208h_1e_1c',
                        title:'百年义利（垡头店）',
                        pos:'清河',
                        price:200
                    },{
                        img:'http://p0.meituan.net/mogu/fc091566222b23c51857ab4316633e43370925.jpg@368w_208h_1e_1c',
                        title:'祈年八号中餐厅',
                        pos:'崇文门新世界',
                        price:98
                    },{
                        img:'http://p0.meituan.net/msmerchant/1a8aaac8cfcf76fae83c2ecd6405bd4c1457315.jpg@368w_208h_1e_1c',
                        title:'北京饭店阳光咖啡厅',
                        pos:'王府井/东单',
                        price:238
                    },{
                        img:'https://img.meituan.net/msmerchant/3fb7c5ebb2e57003dc4a0733568c9683339216.jpg@380w_214h_1e_1c',
                        title:'金掌勺东北菜（王府井店）',
                        pos:'王府井/东单',
                        price:69
                    },{
                        img:'http://p1.meituan.net/wedding/8d26f93de654d433b17774e60a1fc5bd1028431.jpg@240w_180h_1e_1c_1l|watermark=1&&r=2&p=9&x=2&y=2&relative=1&o=20|368w_208h_1e_1c',
                        title:'木北造型（崇文门新世界店)',
                        pos:'崇文门新世界',
                        price:421
                    },{
                        img:'http://p1.meituan.net/dpmerchantalbum/df6753726f5fe30a19139166c7fbe704119922.jpeg@368w_208h_1e_1c',
                        title:'江南赋（内蒙古大厦店）',
                        pos:'王府井/东单',
                        price:114
                    }],
                    spa: [{
                        img:'http://p1.meituan.net/msmerchant/3fb7c5ebb2e57003dc4a0733568c9683339216.jpg@368w_208h_1e_1c',
                        title:'百年义利（垡头店）',
                        pos:'清河',
                        price:200
                    },{
                        img:'http://p0.meituan.net/mogu/fc091566222b23c51857ab4316633e43370925.jpg@368w_208h_1e_1c',
                        title:'祈年八号中餐厅',
                        pos:'崇文门新世界',
                        price:98
                    },{
                        img:'http://p0.meituan.net/msmerchant/1a8aaac8cfcf76fae83c2ecd6405bd4c1457315.jpg@368w_208h_1e_1c',
                        title:'北京饭店阳光咖啡厅',
                        pos:'王府井/东单',
                        price:238
                    },{
                        img:'https://img.meituan.net/msmerchant/3fb7c5ebb2e57003dc4a0733568c9683339216.jpg@380w_214h_1e_1c',
                        title:'金掌勺东北菜（王府井店）',
                        pos:'王府井/东单',
                        price:69
                    },{
                        img:'http://p1.meituan.net/wedding/8d26f93de654d433b17774e60a1fc5bd1028431.jpg@240w_180h_1e_1c_1l|watermark=1&&r=2&p=9&x=2&y=2&relative=1&o=20|368w_208h_1e_1c',
                        title:'木北造型（崇文门新世界店)',
                        pos:'崇文门新世界',
                        price:421
                    },{
                        img:'http://p1.meituan.net/dpmerchantalbum/df6753726f5fe30a19139166c7fbe704119922.jpeg@368w_208h_1e_1c',
                        title:'江南赋（内蒙古大厦店）',
                        pos:'王府井/东单',
                        price:114
                    }],
                    movie: [{
                        img:'http://p1.meituan.net/msmerchant/3fb7c5ebb2e57003dc4a0733568c9683339216.jpg@368w_208h_1e_1c',
                        title:'百年义利（垡头店）',
                        pos:'清河',
                        price:200
                    },{
                        img:'http://p0.meituan.net/mogu/fc091566222b23c51857ab4316633e43370925.jpg@368w_208h_1e_1c',
                        title:'祈年八号中餐厅',
                        pos:'崇文门新世界',
                        price:98
                    },{
                        img:'http://p0.meituan.net/msmerchant/1a8aaac8cfcf76fae83c2ecd6405bd4c1457315.jpg@368w_208h_1e_1c',
                        title:'北京饭店阳光咖啡厅',
                        pos:'王府井/东单',
                        price:238
                    },{
                        img:'https://img.meituan.net/msmerchant/3fb7c5ebb2e57003dc4a0733568c9683339216.jpg@380w_214h_1e_1c',
                        title:'金掌勺东北菜（王府井店）',
                        pos:'王府井/东单',
                        price:69
                    },{
                        img:'http://p1.meituan.net/wedding/8d26f93de654d433b17774e60a1fc5bd1028431.jpg@240w_180h_1e_1c_1l|watermark=1&&r=2&p=9&x=2&y=2&relative=1&o=20|368w_208h_1e_1c',
                        title:'木北造型（崇文门新世界店)',
                        pos:'崇文门新世界',
                        price:421
                    },{
                        img:'http://p1.meituan.net/dpmerchantalbum/df6753726f5fe30a19139166c7fbe704119922.jpeg@368w_208h_1e_1c',
                        title:'江南赋（内蒙古大厦店）',
                        pos:'王府井/东单',
                        price:114
                    }],
                    travel: [{
                        img:'http://p1.meituan.net/msmerchant/3fb7c5ebb2e57003dc4a0733568c9683339216.jpg@368w_208h_1e_1c',
                        title:'百年义利（垡头店）',
                        pos:'清河',
                        price:200
                    },{
                        img:'http://p0.meituan.net/mogu/fc091566222b23c51857ab4316633e43370925.jpg@368w_208h_1e_1c',
                        title:'祈年八号中餐厅',
                        pos:'崇文门新世界',
                        price:98
                    },{
                        img:'http://p0.meituan.net/msmerchant/1a8aaac8cfcf76fae83c2ecd6405bd4c1457315.jpg@368w_208h_1e_1c',
                        title:'北京饭店阳光咖啡厅',
                        pos:'王府井/东单',
                        price:238
                    },{
                        img:'https://img.meituan.net/msmerchant/3fb7c5ebb2e57003dc4a0733568c9683339216.jpg@380w_214h_1e_1c',
                        title:'金掌勺东北菜（王府井店）',
                        pos:'王府井/东单',
                        price:69
                    },{
                        img:'http://p1.meituan.net/wedding/8d26f93de654d433b17774e60a1fc5bd1028431.jpg@240w_180h_1e_1c_1l|watermark=1&&r=2&p=9&x=2&y=2&relative=1&o=20|368w_208h_1e_1c',
                        title:'木北造型（崇文门新世界店)',
                        pos:'崇文门新世界',
                        price:421
                    },{
                        img:'http://p1.meituan.net/dpmerchantalbum/df6753726f5fe30a19139166c7fbe704119922.jpeg@368w_208h_1e_1c',
                        title:'江南赋（内蒙古大厦店）',
                        pos:'王府井/东单',
                        price:114
                    }]                    
                },                

            }
        },
        computed: {
            cur:function() {
                return  this.list[this.kind]
            }
        },
        methods: {
            over:function(e) {
                console.log('over...')
                let dom = e.target
                let tag = dom.tagName.toLowerCase()
                let self = this
                console.log(dom)
                if(tag == 'dd'){
                    this.kind = dom.getAttribute('kind')
                }
            },

        }
    }
</script>
