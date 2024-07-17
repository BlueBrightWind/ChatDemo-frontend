<template>
    <div class="sidebar-container">
        <div class="avatar-content">
            <el-avatar class="avatar-item" src="https://avatars.githubusercontent.com/u/38139389?v=4"></el-avatar>
        </div>
        <div class="sidebar-btn-content">
            <el-button :icon="Comment" class="btn-item selected"></el-button>
            <el-button :icon="UserFilled" class="btn-item"></el-button>
        </div>
        <div class="sidebar-setting-content">
            <el-button :icon="Tools" class="setting-btn-item"></el-button>
        </div>
    </div>
</template>

<script setup>
import { Comment, UserFilled, Tools } from '@element-plus/icons-vue'
</script>

<script>
export default {
    name: 'SideBar',
    data() {
        return {

        }
    }

}
</script>


<style lang="scss" scoped>
.sidebar-container {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;

    .avatar-content {
        margin-top: 10px;
        width: 100%;
        height: 70px;
        display: flex;
        justify-content: center;
        align-items: center;

        .avatar-item {
            width: 45px;
            height: 45px;
        }
    }

    .sidebar-btn-content {
        flex: 1;
        width: 100%;
        height: 0;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: left;

        .btn-item {
            width: 40px;
            height: 40px;
            margin: 0;
            font-size: 20px;
            margin-top: 10px;
            border: 0;
            outline: none;
            color: var(--el-text-color-regular);
        }

        .btn-item:hover {
            background-color: var(--el-color-info-light-8);
            color: var(--el-text-color-regular);
        }

        .btn-item.selected {
            background-color: var(--el-color-info-light-8);
            color: var(--el-button-hover-text-color);
        }

    }

    .sidebar-setting-content {
        width: 100%;
        height: 70px;
        display: flex;
        justify-content: center;
        align-items: center;

        .setting-btn-item {
            width: 40px;
            height: 40px;
            margin: 0;
            font-size: 20px;
            margin-top: 10px;
            border: 0;
            outline: none;
            color: var(--el-text-color-regular);
        }

        .setting-btn-item:hover {
            background-color: var(--el-color-info-light-8);
            color: var(--el-text-color-regular);
        }
    }
}
</style>
