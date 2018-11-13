<template>
    <div class="m-nav">
        <ul class="nav">
            <li class="list">
                <nuxt-link to='/my'>我的美团</nuxt-link>
                <dl>
                    <dd><nuxt-link to='/my'>我的订单</nuxt-link></dd>
                    <dd><nuxt-link to='/my'>我的收藏</nuxt-link></dd>
                    <dd><nuxt-link to='/my'>抵用券</nuxt-link></dd>
                    <dd><nuxt-link to='/my'>账户设置</nuxt-link></dd>
                </dl>
            </li>
            <li class=""><nuxt-link to='/my'>手机APP</nuxt-link></li>
            <li class="list bd">
                <nuxt-link to='/center'>商家中心</nuxt-link>
                <dl>
                    <dd><nuxt-link to='/my'>登录商家中心</nuxt-link></dd>
                    <dd><nuxt-link to='/my'>美团智能收银</nuxt-link></dd>
                    <dd><nuxt-link to='/my'>我想合作</nuxt-link></dd>
                    <dd><nuxt-link to='/my'>手机免费开店</nuxt-link></dd>
                    <dd><nuxt-link to='/my'>餐饮代理商招募</nuxt-link></dd>
                    <dd><nuxt-link to='/my'>商家申请开票</nuxt-link></dd>
                </dl>
            </li>
            <li class="list site">
                <nuxt-link to='/site'>网站导航</nuxt-link>
                <div class="subContainer">
                    <dl class="hotel">
                        <dd>1</dd>
                    </dl>
                    <dl class="food">
                        <dd>2</dd>
                    </dl>
                    <dl class="movie">
                        <dd>3</dd>
                    </dl>
                    <dl class="app">
                        <dd>4</dd>
                    </dl>
                </div>
            </li>
        </ul>
    </div>
</template>
<script>
export default {
    
}
</script>
<style lang='scss'>

</style>


