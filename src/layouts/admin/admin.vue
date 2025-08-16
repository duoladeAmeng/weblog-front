<script setup>
import AdminFooter from './components/AdminFooter.vue';
import AdminHeader from './components/AdminHeader.vue';
import AdminMenu from './components/AdminMenu.vue';
import AdminTagList from './components/AdminTagList.vue';
</script>

<template>
    <el-container>
        <el-aside> <AdminMenu></AdminMenu> </el-aside>
        <el-container>
             <!-- 顶栏容器 -->
            <el-header>
                <AdminHeader></AdminHeader>
            </el-header>
            
            <el-main>
                <AdminTagList></AdminTagList>
                <!-- 主内容（根据路由动态展示不同页面） -->
                <router-view></router-view>
            </el-main>
            
            <!-- 底栏容器 -->
            <el-footer>
                <AdminFooter></AdminFooter>
            </el-footer>
        </el-container>
    </el-container>
</template>
<style>

</style>