<template>
    <el-container class="add-notice-container">
        <el-header class="add-notice-title">
            <div class="add-notice-title-content">
                <el-button class="title-return-btn" :icon="Back" />
                <div class="title-notice">好友通知列表</div>
                <el-button class="title-delete-btn" :icon="Delete" />
            </div>
        </el-header>
        <el-main class="add-notice-content">
            <el-scrollbar class="add-notice-content-inner">
                <!-- 通知开始 -->
                <div class="notice-item">
                    <div class="notice-avatar">
                        <el-avatar style="background-color: var(--color-dark-2);">小明</el-avatar>
                    </div>
                    <div class="notice-info">
                        <div class="friend-name">小明aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa</div>
                        <div class="friend-remark">你好，我是小明aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa</div>
                    </div>
                    <div class="notice-process">
                        <el-button class="notice-process-btn">同意</el-button>
                        <el-button class="notice-process-btn">拒绝</el-button>
                    </div>
                    <div class="notice-process-result">
                        <div class="notice-process-result-item">已同意</div>
                        <div class="notice-process-result-item">已拒绝</div>
                    </div>
                </div>
                <!-- 通知结束 -->
                <!-- 测试开始 -->
                <div class="notice-item">
                    <div class="notice-avatar">
                        <el-avatar style="background-color: var(--color-dark-2);">小明</el-avatar>
                    </div>
                    <div class="notice-info">
                        <div class="friend-name">小明</div>
                        <div class="friend-remark">你好，我是小明</div>
                    </div>
                    <div class="notice-process">
                        <el-button class="notice-process-btn">同意</el-button>
                        <el-button class="notice-process-btn">拒绝</el-button>
                    </div>
                </div>
                <div class="notice-item">
                    <div class="notice-avatar">
                        <el-avatar style="background-color: var(--color-dark-2);">小明</el-avatar>
                    </div>
                    <div class="notice-info">
                        <div class="friend-name">小明</div>
                        <div class="friend-remark">你好，我是小明</div>
                    </div>
                    <div class="notice-process-result">
                        <div class="notice-process-result-item">已同意</div>
                    </div>
                </div>
                <div class="notice-item">
                    <div class="notice-avatar">
                        <el-avatar style="background-color: var(--color-dark-2);">小明</el-avatar>
                    </div>
                    <div class="notice-info">
                        <div class="friend-name">小明</div>
                        <div class="friend-remark">你好，我是小明</div>
                    </div>
                    <div class="notice-process-result">
                        <div class="notice-process-result-item">已拒绝</div>
                    </div>
                </div>
                <!-- 测试结束 -->
            </el-scrollbar>
        </el-main>
    </el-container>
</template>

<script setup>
import { Back, Delete } from '@element-plus/icons-vue'
</script>

<script>
export default {
    name: 'AddNotice',
    data() {
        return {

        }
    },
    methods: {

    }

}
</script>

<style lang="scss" scoped>
.add-notice-container {
    width: 100%;
    height: 100%;
    background-color: var(--el-bg-color-page);

    .add-notice-title {
        height: 65px;
        width: 100%;
        margin-top: 10px;

        .add-notice-title-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 100%;

            .title-return-btn {
                outline: none;
                border: none;
                background-color: transparent;
                font-size: 20px;
                width: 30px;
                height: 30px;
            }

            .title-delete-btn {
                outline: none;
                border: none;
                background-color: transparent;
                font-size: 20px;
                width: 30px;
                height: 30px;
            }
        }
    }

    .add-notice-content {
        width: 100%;
        padding: 0;
        padding-left: 20px;

        .add-notice-content-inner {
            width: calc(100% - 20px);
            padding-right: 20px;

            :deep(.el-scrollbar__view) {
                display: flex;
                flex-direction: column;
                align-items: center;
            }

            .notice-item {
                display: flex;
                align-items: center;
                width: 90%;
                max-width: 600px;
                height: 40px;
                background-color: var(--el-bg-color);
                padding: 15px;
                border-radius: 10px;
                margin-top: 20px;

                .notice-avatar {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    flex-shrink: 0;
                }

                .notice-info {
                    margin-left: 10px;
                    flex: 1;
                    height: 100%;
                    display: flex;
                    flex-direction: column;
                    justify-content: space-between;
                    width: 0;

                    .friend-name {
                        height: 20px;
                        line-height: 20px;
                        font-size: 14px;
                        overflow: hidden;
                        text-overflow: ellipsis;
                        white-space: nowrap;
                    }

                    .friend-remark {
                        height: 20px;
                        line-height: 20px;
                        overflow: hidden;
                        font-size: 13px;
                        color: var(--el-color-info);
                        overflow: hidden;
                        text-overflow: ellipsis;
                        white-space: nowrap;
                    }
                }

                .notice-process {
                    flex-shrink: 0;

                    .notice-process-btn {
                        height: 25px;
                        font-size: 13px;
                        background-color: transparent;
                    }
                }

                .notice-process-result {
                    flex-shrink: 0;

                    .notice-process-result-item {
                        height: 20px;
                        font-size: 13px;
                        color: var(--el-color-info);
                    }
                }
            }
        }


    }
}
</style>