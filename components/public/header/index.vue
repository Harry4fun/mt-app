<template>
    <div class="m-header">
        <el-row>
            <el-col>
                <top-bar />
            </el-col>
        </el-row>
        <el-row>
            <el-col>
                <search-bar />
            </el-col>
        </el-row>        
    </div>
</template>
<script>
import searchBar from './searchbar.vue'
import topBar from './topbar.vue'
export default {
    components: {
    searchBar,topBar
    }
}
</script>

<style lang="scss">
@import "@/assets/css/public/header/index.scss"
</style>
