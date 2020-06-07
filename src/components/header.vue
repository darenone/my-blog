<template>
    <header>
        <div class="wrapper">
            <el-row>
                <el-col :span="4">
                    <div class="logo">宗强的博客</div>
                </el-col>
                <el-col :span="20">
                    <el-menu 
                    :default-active="activeIndex" 
                    class="menu-list" 
                    mode="horizontal" 
                    @select="handleSelect"
                    background-color="#2d2d2d"
                    text-color="#9d9d9d"
                    active-text-color="#fff">
                        <el-menu-item index="1">
                            <router-link 
                            to="/">首页</router-link>
                        </el-menu-item>
                        <el-menu-item index="2">
                            <router-link to="/">我的博客</router-link>
                        </el-menu-item>
                        <el-menu-item index="3">
                            <router-link to="/">登录</router-link>
                        </el-menu-item>
                    </el-menu>
                </el-col>
            </el-row>
        </div>
    </header>
</template>
<script>
export default {
    data () {
        return {
            activeIndex: '1'
        }
    },
    methods: {
        handleSelect (index) {
            this.activeIndex = index + ''
        }
    }
}
</script>
