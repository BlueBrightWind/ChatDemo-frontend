<template>
    <el-container class="friend-container">
        <el-header class="search-container">
            <el-container style="width: 100%; height: 100%;">
                <el-aside class="search-input">
                    <el-input v-model="input1" placeholder="搜索" :prefix-icon="Search" />
                </el-aside>
                <el-main class="search-add-friend">
                    <CirclePlusFilled />
                </el-main>
            </el-container>
        </el-header>
        <el-main class="friendlist-container">
            <el-scrollbar class="friendlist-container-inner">
                <!-- 好友信息开始 -->
                <div class="friend selected">
                    <div class="friend-avatar">
                        <el-avatar
                            style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小明</el-avatar>
                    </div>
                    <div class="friend-info">
                        <div class="friend-name">
                            <div class="online-status status-online"></div>
                            <div class="name-content">小明</div>
                        </div>
                        <div class="friend-latest-message">
                            <span class="friend-latest-message-item">优先处理日构建事务</span>
                        </div>
                    </div>
                    <div class="message-time">
                        <span>Today</span>
                        <span>17:24</span>
                    </div>
                </div>
                <!-- 好友信息结束 -->
                <!-- 好友信息开始 -->
                <div class="friend">
                    <div class="friend-avatar">
                        <el-avatar
                            style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小笨</el-avatar>
                    </div>
                    <div class="friend-info">
                        <div class="friend-name">
                            <div class="online-status status-offline"></div>
                            <div class="name-content">小笨</div>
                        </div>
                        <div class="friend-latest-message">
                            <span class="friend-latest-message-item">优先处理日构建事务</span>
                        </div>
                    </div>
                    <div class="message-time">
                        <span>2020-12-24</span>
                        <span>14:32</span>
                    </div>
                </div>
                <!-- 好友信息结束 -->
                <!-- 测试开始 -->
                <div class="friend">
                    <div class="friend-avatar">
                        <el-avatar
                            style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小笨</el-avatar>
                    </div>
                    <div class="friend-info">
                        <div class="friend-name">
                            <div class="online-status status-offline"></div>
                            <div class="name-content">小笨</div>
                        </div>
                        <div class="friend-latest-message">
                            <span class="friend-latest-message-item">优先处理日构建事务</span>
                        </div>
                    </div>
                    <div class="message-time">
                        <span>2020-12-24</span>
                        <span>14:32</span>
                    </div>
                </div>
                <div class="friend">
                    <div class="friend-avatar">
                        <el-avatar
                            style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小笨</el-avatar>
                    </div>
                    <div class="friend-info">
                        <div class="friend-name">
                            <div class="online-status status-offline"></div>
                            <div class="name-content">小笨</div>
                        </div>
                        <div class="friend-latest-message">
                            <span class="friend-latest-message-item">优先处理日构建事务</span>
                        </div>
                    </div>
                    <div class="message-time">
                        <span>2020-12-24</span>
                        <span>14:32</span>
                    </div>
                </div>
                <div class="friend">
                    <div class="friend-avatar">
                        <el-avatar
                            style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小笨</el-avatar>
                    </div>
                    <div class="friend-info">
                        <div class="friend-name">
                            <div class="online-status status-offline"></div>
                            <div class="name-content">小笨</div>
                        </div>
                        <div class="friend-latest-message">
                            <span class="friend-latest-message-item">优先处理日构建事务</span>
                        </div>
                    </div>
                    <div class="message-time">
                        <span>2020-12-24</span>
                        <span>14:32</span>
                    </div>
                </div>
                <div class="friend">
                    <div class="friend-avatar">
                        <el-avatar
                            style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小笨</el-avatar>
                    </div>
                    <div class="friend-info">
                        <div class="friend-name">
                            <div class="online-status status-offline"></div>
                            <div class="name-content">小笨</div>
                        </div>
                        <div class="friend-latest-message">
                            <span class="friend-latest-message-item">优先处理日构建事务</span>
                        </div>
                    </div>
                    <div class="message-time">
                        <span>2020-12-24</span>
                        <span>14:32</span>
                    </div>
                </div>
                <div class="friend">
                    <div class="friend-avatar">
                        <el-avatar
                            style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小笨</el-avatar>
                    </div>
                    <div class="friend-info">
                        <div class="friend-name">
                            <div class="online-status status-offline"></div>
                            <div class="name-content">小笨</div>
                        </div>
                        <div class="friend-latest-message">
                            <span class="friend-latest-message-item">优先处理日构建事务</span>
                        </div>
                    </div>
                    <div class="message-time">
                        <span>2020-12-24</span>
                        <span>14:32</span>
                    </div>
                </div>
                <div class="friend">
                    <div class="friend-avatar">
                        <el-avatar
                            style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小笨</el-avatar>
                    </div>
                    <div class="friend-info">
                        <div class="friend-name">
                            <div class="online-status status-offline"></div>
                            <div class="name-content">小笨</div>
                        </div>
                        <div class="friend-latest-message">
                            <span class="friend-latest-message-item">优先处理日构建事务</span>
                        </div>
                    </div>
                    <div class="message-time">
                        <span>2020-12-24</span>
                        <span>14:32</span>
                    </div>
                </div>
                <div class="friend">
                    <div class="friend-avatar">
                        <el-avatar
                            style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小笨</el-avatar>
                    </div>
                    <div class="friend-info">
                        <div class="friend-name">
                            <div class="online-status status-offline"></div>
                            <div class="name-content">小笨</div>
                        </div>
                        <div class="friend-latest-message">
                            <span class="friend-latest-message-item">优先处理日构建事务</span>
                        </div>
                    </div>
                    <div class="message-time">
                        <span>2020-12-24</span>
                        <span>14:32</span>
                    </div>
                </div>
                <!-- 测试结束 -->
            </el-scrollbar>

        </el-main>
    </el-container>
</template>

<script setup>
import { Search } from '@element-plus/icons-vue'
import { CirclePlusFilled } from '@element-plus/icons-vue'
</script>

<script>
export default {
    name: 'FriendList',

}
</script>


<style lang="scss" scoped>
.friend-container {
    width: 300px;
    height: 100%;
    border-right: 1px solid var(--el-border-color-extra-light);

    .search-container {
        margin-top: 10px;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        height: 60px;

        .search-input {
            width: 85%;
            height: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .search-input :deep(.el-input__wrapper) {
            border-radius: 999999px;
            height: 35px;
        }

        .search-add-friend {
            width: 15%;
            height: 100%;
            display: flex;
            justify-content: right;
            align-items: center;
            padding: 0;
        }

        .search-add-friend :deep(svg) {
            width: 70%;
            height: 70%;
            color: var(--color-base);
        }
    }

    .friendlist-container {
        padding: 12px;
        padding-right: 0;

        .friendlist-container-inner {
            padding-right: 12px;

            .friend {
                width: 100%;
                height: 65px;
                border-radius: 5px;
                display: flex;
                align-items: center;
                user-select: none;
                padding-top: 7px;
                padding-bottom: 7px;

                .friend-avatar {
                    width: 65px;
                    height: 65px;
                    display: flex;
                    justify-content: center;
                    align-items: center;
                }

                .friend-info {
                    width: calc(100% - 65px - 80px);
                    height: 100%;
                    display: flex;
                    flex-direction: column;
                    justify-content: center;

                    .friend-name {
                        width: 100%;
                        height: 35%;
                        display: flex;
                        justify-content: center;
                        align-items: center;

                        .online-status {
                            width: 10px;
                            height: 10px;
                            border-radius: 50%;
                            display: flex;
                            justify-content: center;
                            align-items: center;
                        }

                        .name-content {
                            flex: 1;
                            height: 100%;
                            display: flex;
                            justify-content: left;
                            align-items: center;
                            padding-left: 5px;
                            line-height: 100%;
                            font-size: 15px;
                        }

                        .status-online {
                            background-color: #4caf50;
                        }

                        .status-offline {
                            background-color: #9e9e9e;
                        }

                    }

                    .friend-latest-message {
                        width: 100%;
                        height: 30%;
                        display: flex;
                        justify-content: left;
                        align-items: center;

                        .friend-latest-message-item {
                            white-space: nowrap;
                            overflow: hidden;
                            text-overflow: ellipsis;
                            font-size: 11px;
                            color: var(--el-color-info);
                        }
                    }
                }

                .message-time {
                    width: 80px;
                    height: 100%;
                    color: var(--el-color-info);
                    font-size: 11px;
                    display: flex;
                    flex-direction: column;
                    justify-content: center;
                    align-items: center;
                }
            }

            .friend:hover {
                background-color: var(--el-color-info-light-9);
            }

            .friend.selected {
                background-color: var(--el-color-primary-light-8);
            }
        }
    }

}
</style>
