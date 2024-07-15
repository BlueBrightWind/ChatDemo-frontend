<template>
    <div class="add-friend-container">
        <el-container style="width: 100%; height: 100%;">
            <el-header class="add-friend-search">
                <el-input v-model="inputValue" placeholder="搜索" :prefix-icon="Search" />
            </el-header>
            <el-main class="friend-search-result">
                <el-tabs v-model="activeName" @tab-click="handleClick" style="width: 100%; height: 100%;">
                    <el-tab-pane label="全部" name="全部" style="width: 100%; height: 100%;">
                        <el-scrollbar class="friend-search-result-inner">
                            <div class="friend-type-results">
                                <div class="friend-type">用户</div>
                                <div class="friend-list">
                                    <!-- 好友开始 -->
                                    <div class="friend">
                                        <el-avatar class="friend-avatar">小明</el-avatar>
                                        <div class="friend-info">
                                            <div class="friend-name">
                                                <div class="name-item">
                                                    小明aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
                                                </div>
                                            </div>
                                            <div class="friend-desc">
                                                <div class="desc-item">
                                                    个性签名aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
                                                </div>
                                            </div>
                                        </div>
                                        <div class="add-button">
                                            <el-button class="button-item">添加</el-button>
                                        </div>
                                    </div>
                                    <!-- 好友结束 -->
                                    <!-- 测试开始 -->
                                    <div class="friend">
                                        <el-avatar class="friend-avatar">小明</el-avatar>
                                        <div class="friend-info">
                                            <div class="friend-name">
                                                <div class="name-item">
                                                    小明
                                                </div>
                                            </div>
                                            <div class="friend-desc">
                                                <div class="desc-item">
                                                    个性签名
                                                </div>
                                            </div>
                                        </div>
                                        <div class="add-button">
                                            <el-button class="button-item">添加</el-button>
                                        </div>
                                    </div>
                                    <div class="friend">
                                        <el-avatar class="friend-avatar">小明</el-avatar>
                                        <div class="friend-info">
                                            <div class="friend-name">
                                                <div class="name-item">
                                                    小明
                                                </div>
                                            </div>
                                            <div class="friend-desc">
                                                <div class="desc-item">
                                                    个性签名
                                                </div>
                                            </div>
                                        </div>
                                        <div class="add-button">
                                            <el-button class="button-item">添加</el-button>
                                        </div>
                                    </div>
                                    <div class="friend">
                                        <el-avatar class="friend-avatar">小明</el-avatar>
                                        <div class="friend-info">
                                            <div class="friend-name">
                                                <div class="name-item">
                                                    小明
                                                </div>
                                            </div>
                                            <div class="friend-desc">
                                                <div class="desc-item">
                                                    个性签名
                                                </div>
                                            </div>
                                        </div>
                                        <div class="add-button">
                                            <el-button class="button-item">添加</el-button>
                                        </div>
                                    </div>
                                    <div class="friend">
                                        <el-avatar class="friend-avatar">小明</el-avatar>
                                        <div class="friend-info">
                                            <div class="friend-name">
                                                <div class="name-item">
                                                    小明
                                                </div>
                                            </div>
                                            <div class="friend-desc">
                                                <div class="desc-item">
                                                    个性签名
                                                </div>
                                            </div>
                                        </div>
                                        <div class="add-button">
                                            <el-button class="button-item">添加</el-button>
                                        </div>
                                    </div>
                                    <div class="friend">
                                        <el-avatar class="friend-avatar">小明</el-avatar>
                                        <div class="friend-info">
                                            <div class="friend-name">
                                                <div class="name-item">
                                                    小明
                                                </div>
                                            </div>
                                            <div class="friend-desc">
                                                <div class="desc-item">
                                                    个性签名
                                                </div>
                                            </div>
                                        </div>
                                        <div class="add-button">
                                            <el-button class="button-item">添加</el-button>
                                        </div>
                                    </div>
                                    <div class="friend">
                                        <el-avatar class="friend-avatar">小明</el-avatar>
                                        <div class="friend-info">
                                            <div class="friend-name">
                                                <div class="name-item">
                                                    小明
                                                </div>
                                            </div>
                                            <div class="friend-desc">
                                                <div class="desc-item">
                                                    个性签名
                                                </div>
                                            </div>
                                        </div>
                                        <div class="add-button">
                                            <el-button class="button-item">添加</el-button>
                                        </div>
                                    </div>
                                    <div class="friend">
                                        <el-avatar class="friend-avatar">小明</el-avatar>
                                        <div class="friend-info">
                                            <div class="friend-name">
                                                <div class="name-item">
                                                    小明
                                                </div>
                                            </div>
                                            <div class="friend-desc">
                                                <div class="desc-item">
                                                    个性签名
                                                </div>
                                            </div>
                                        </div>
                                        <div class="add-button">
                                            <el-button class="button-item">添加</el-button>
                                        </div>
                                    </div>
                                    <div class="friend">
                                        <el-avatar class="friend-avatar">小明</el-avatar>
                                        <div class="friend-info">
                                            <div class="friend-name">
                                                <div class="name-item">
                                                    小明
                                                </div>
                                            </div>
                                            <div class="friend-desc">
                                                <div class="desc-item">
                                                    个性签名
                                                </div>
                                            </div>
                                        </div>
                                        <div class="add-button">
                                            <el-button class="button-item">添加</el-button>
                                        </div>
                                    </div>
                                    <div class="friend">
                                        <el-avatar class="friend-avatar">小明</el-avatar>
                                        <div class="friend-info">
                                            <div class="friend-name">
                                                <div class="name-item">
                                                    小明
                                                </div>
                                            </div>
                                            <div class="friend-desc">
                                                <div class="desc-item">
                                                    个性签名
                                                </div>
                                            </div>
                                        </div>
                                        <div class="add-button">
                                            <el-button class="button-item">添加</el-button>
                                        </div>
                                    </div>
                                    <!-- 测试结束 -->
                                </div>
                            </div>
                            <div class="friend-type-results">
                                <div class="friend-type">群聊</div>
                                <div class="friend-list">
                                    <!-- 测试开始 -->
                                    <div class="friend">
                                        <el-avatar class="friend-avatar">小明</el-avatar>
                                        <div class="friend-info">
                                            <div class="friend-name">
                                                <div class="name-item">
                                                    原神启动
                                                </div>
                                            </div>
                                            <div class="friend-desc">
                                                <div class="desc-item">
                                                    原神启动
                                                </div>
                                            </div>
                                        </div>
                                        <div class="add-button">
                                            <el-button class="button-item">添加</el-button>
                                        </div>
                                    </div>
                                    <div class="friend">
                                        <el-avatar class="friend-avatar">小明</el-avatar>
                                        <div class="friend-info">
                                            <div class="friend-name">
                                                <div class="name-item">
                                                    原神启动
                                                </div>
                                            </div>
                                            <div class="friend-desc">
                                                <div class="desc-item">
                                                    原神启动
                                                </div>
                                            </div>
                                        </div>
                                        <div class="add-button">
                                            <el-button class="button-item">添加</el-button>
                                        </div>
                                    </div>
                                    <div class="friend">
                                        <el-avatar class="friend-avatar">小明</el-avatar>
                                        <div class="friend-info">
                                            <div class="friend-name">
                                                <div class="name-item">
                                                    原神启动
                                                </div>
                                            </div>
                                            <div class="friend-desc">
                                                <div class="desc-item">
                                                    原神启动
                                                </div>
                                            </div>
                                        </div>
                                        <div class="add-button">
                                            <el-button class="button-item">添加</el-button>
                                        </div>
                                    </div>
                                    <div class="friend">
                                        <el-avatar class="friend-avatar">小明</el-avatar>
                                        <div class="friend-info">
                                            <div class="friend-name">
                                                <div class="name-item">
                                                    原神启动
                                                </div>
                                            </div>
                                            <div class="friend-desc">
                                                <div class="desc-item">
                                                    原神启动
                                                </div>
                                            </div>
                                        </div>
                                        <div class="add-button">
                                            <el-button class="button-item">添加</el-button>
                                        </div>
                                    </div>
                                    <div class="friend">
                                        <el-avatar class="friend-avatar">小明</el-avatar>
                                        <div class="friend-info">
                                            <div class="friend-name">
                                                <div class="name-item">
                                                    原神启动
                                                </div>
                                            </div>
                                            <div class="friend-desc">
                                                <div class="desc-item">
                                                    原神启动
                                                </div>
                                            </div>
                                        </div>
                                        <div class="add-button">
                                            <el-button class="button-item">添加</el-button>
                                        </div>
                                    </div>
                                    <div class="friend">
                                        <el-avatar class="friend-avatar">小明</el-avatar>
                                        <div class="friend-info">
                                            <div class="friend-name">
                                                <div class="name-item">
                                                    原神启动
                                                </div>
                                            </div>
                                            <div class="friend-desc">
                                                <div class="desc-item">
                                                    原神启动
                                                </div>
                                            </div>
                                        </div>
                                        <div class="add-button">
                                            <el-button class="button-item">添加</el-button>
                                        </div>
                                    </div>
                                    <div class="friend">
                                        <el-avatar class="friend-avatar">小明</el-avatar>
                                        <div class="friend-info">
                                            <div class="friend-name">
                                                <div class="name-item">
                                                    原神启动
                                                </div>
                                            </div>
                                            <div class="friend-desc">
                                                <div class="desc-item">
                                                    原神启动
                                                </div>
                                            </div>
                                        </div>
                                        <div class="add-button">
                                            <el-button class="button-item">添加</el-button>
                                        </div>
                                    </div>
                                    <div class="friend">
                                        <el-avatar class="friend-avatar">小明</el-avatar>
                                        <div class="friend-info">
                                            <div class="friend-name">
                                                <div class="name-item">
                                                    原神启动
                                                </div>
                                            </div>
                                            <div class="friend-desc">
                                                <div class="desc-item">
                                                    原神启动
                                                </div>
                                            </div>
                                        </div>
                                        <div class="add-button">
                                            <el-button class="button-item">添加</el-button>
                                        </div>
                                    </div>
                                    <div class="friend">
                                        <el-avatar class="friend-avatar">小明</el-avatar>
                                        <div class="friend-info">
                                            <div class="friend-name">
                                                <div class="name-item">
                                                    原神启动
                                                </div>
                                            </div>
                                            <div class="friend-desc">
                                                <div class="desc-item">
                                                    原神启动
                                                </div>
                                            </div>
                                        </div>
                                        <div class="add-button">
                                            <el-button class="button-item">添加</el-button>
                                        </div>
                                    </div>
                                    <div class="friend">
                                        <el-avatar class="friend-avatar">小明</el-avatar>
                                        <div class="friend-info">
                                            <div class="friend-name">
                                                <div class="name-item">
                                                    原神启动
                                                </div>
                                            </div>
                                            <div class="friend-desc">
                                                <div class="desc-item">
                                                    原神启动
                                                </div>
                                            </div>
                                        </div>
                                        <div class="add-button">
                                            <el-button class="button-item">添加</el-button>
                                        </div>
                                    </div>
                                    <!-- 测试结束 -->
                                </div>
                            </div>
                        </el-scrollbar>
                    </el-tab-pane>
                    <el-tab-pane label="用户" name="用户">Config</el-tab-pane>
                    <el-tab-pane label="群聊" name="群聊">Role</el-tab-pane>
                </el-tabs>
            </el-main>
        </el-container>

    </div>
</template>

<script setup>
import { Search } from '@element-plus/icons-vue'
</script>

<script>
export default {
    name: 'AddFriend',
}
</script>

<style lang="scss" scoped>
.add-friend-container {
    width: 600px;
    height: 700px;
    border-radius: 5px;
    background-color: var(--el-bg-color-page);

    .add-friend-search {
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;

        :deep(.el-input__wrapper) {
            border-radius: 999999px;
            height: 35px;
        }
    }

    .friend-search-result {
        padding: 0;
        overflow: hidden;

        :deep(.el-tabs__header) {
            padding-left: 20px;
            padding-right: 20px;
        }

        :deep(.el-tabs__content) {
            padding-left: 20px;
            border-top: 1px solid var(--el-border-color-light);
            width: calc(100% - 20px);
            height: calc(100% - 40px - 15px - 1px);
        }

        .friend-search-result-inner {
            width: 100%;
            height: 100%;

            :deep(.el-scrollbar__wrap) {
                padding-right: 20px;
            }

            .friend-type-results {
                width: 100%;
                display: flex;
                flex-direction: column;

                .friend-type {
                    width: 100%;
                    height: 30px;
                    color: var(--el-color-info-light-3);
                    font-size: 13px;
                    line-height: 30px;
                }

                .friend-list {
                    width: 100%;
                    height: 100%;
                    border-radius: 5px;

                    .friend {
                        width: 100%;
                        height: 40px;
                        padding-top: 10px;
                        padding-bottom: 10px;
                        display: flex;

                        .friend-avatar {
                            display: flex;
                            justify-content: center;
                            align-items: center;
                            width: 40px;
                            height: 40px;
                            border-radius: 50%;
                            margin-right: 10px;
                            background-color: var(--color-dark-2);
                        }

                        .friend-info {
                            flex: 1;
                            overflow: hidden;
                            display: flex;
                            flex-direction: column;
                            justify-content: space-between;

                            .friend-name {
                                display: flex;
                                justify-content: left;
                                align-items: center;

                                .name-item {
                                    font-size: 14px;
                                    color: var(--el-text-color-primary);
                                    overflow: hidden;
                                    text-overflow: ellipsis;
                                    white-space: nowrap;
                                }

                            }

                            .friend-desc {
                                display: flex;
                                justify-content: left;
                                align-items: center;

                                .desc-item {
                                    font-size: 14px;
                                    color: var(--el-text-color-secondary);
                                    overflow: hidden;
                                    text-overflow: ellipsis;
                                    white-space: nowrap;
                                }

                            }
                        }

                        .add-button {
                            display: flex;
                            width: 100px;
                            justify-content: center;
                            align-items: center;

                            .button-item {
                                width: 70px;
                                height: 25px;
                            }
                        }
                    }
                }
            }
        }
    }
}
</style>