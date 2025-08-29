<script>
import {defineComponent} from "vue";
import {ArrowDown, Fold, FullScreen} from "@element-plus/icons-vue";

export default defineComponent({
  components: {ArrowDown, Fold, FullScreen}
})
</script>
<template>
    <!-- <div bg-emerald-700  text-white>头部</div> -->
    <div class="bg-white h-[64px] text-white flex pr-4 border-b border-slate-200">

      <!-- 左边栏收缩、展开 -->
      <div class="w-[42px] h-[64px] cursor-pointer flex items-center justify-center text-gray-700 hover:bg-gray-200">
        <el-icon>
          <Fold />
        </el-icon>
      </div>



      <div class="ml-auto flex">

        <!-- 点击全屏展示 -->

        <el-tooltip
            class="box-item"
            effect="dark"
            content="全屏"
            placement="bottom"
        >
          <div class="w-[42px] h-[64px] cursor-pointer flex items-center justify-center text-gray-700 mr-2 hover:bg-gray-200">
            <el-icon>
              <FullScreen />
            </el-icon>
          </div>
        </el-tooltip>


<!--        登录用户头像-->
        <el-dropdown>
            <span class="el-dropdown-link flex items-center justify-center text-gray-700 text-xs">

              <el-avatar class="mr-2" size="25"></el-avatar>
              Admin
              <el-icon class="el-icon--right">
                <arrow-down />
              </el-icon>
            </span>
            <template #dropdown>
              <el-dropdown-menu>
                <el-dropdown-item>修改密码</el-dropdown-item>
                <el-dropdown-item>退出登录</el-dropdown-item>
              </el-dropdown-menu>
            </template>
        </el-dropdown>



      </div>


    </div>
</template>
<style>
</style>