<template>
    <el-container class="message-container">
        <el-header class="search-container">
            <el-container style="width: 100%; height: 100%;">
                <el-aside class="search-input">
                    <el-input v-model="filterInput" placeholder="搜索" :prefix-icon="Search" />
                </el-aside>
                <el-main class="search-add-friend">
                    <CirclePlusFilled @click.stop="openAddList" />
                    <div v-show="controlInfo.showAddList" class="add-list">
                        <div class="list-item">
                            <div class="list-item-content">
                                <el-icon class="list-item-icon">
                                    <ChatDotSquare />
                                </el-icon>
                                发起群聊
                            </div>
                        </div>
                        <div class="list-item">
                            <div class="list-item-content">
                                <el-icon class="list-item-icon">
                                    <User />
                                </el-icon>
                                添加好友/群
                            </div>
                        </div>
                    </div>
                </el-main>
            </el-container>
        </el-header>
        <el-main class="messagelist-container">
            <el-scrollbar class="messagelist-container-inner">
                <div v-for="message, index in filterlist" class="message"
                    :class="{ selected: controlInfo.selectId == message.key }" @click="handleSelect(message.key)">
                    <div class="message-avatar">
                        <el-avatar style="width: 75%; height: 75%; background-color: var(--color-dark-2);">{{
                            message.name.substring(message.name.length - 2) }}</el-avatar>
                    </div>
                    <div class="message-info">
                        <div class="message-name">
                            <div class="name-content">{{ message.name }}</div>
                        </div>
                        <div class="message-latest-message">
                            <span class="message-latest-message-item">{{ message.latestMessage }}</span>
                        </div>
                    </div>
                    <div class="message-time">
                        <span>{{ timestrapToDate(message.time) }}</span>
                        <span>{{ timestrapToTime(message.time) }}</span>
                    </div>
                </div>
            </el-scrollbar>

        </el-main>
    </el-container>
</template>

<script setup>
import { Search } from '@element-plus/icons-vue'
import { CirclePlusFilled, User, ChatDotSquare } from '@element-plus/icons-vue'
import { onMounted, getCurrentInstance } from 'vue'

const ins = getCurrentInstance();

onMounted(() => {
    // 点击任意位置关闭添加好友列表
    document.addEventListener('click', () => {
        ins.data.controlInfo.showAddList = false;
    })
})
</script>

<script>
export default {
    name: 'messageList',
    data() {
        return {
            filterInput: '',
            controlInfo: {
                showAddList: false,
                selectId: 0
            },
            messagelist: [
                {
                    key: 1,
                    id: 1,
                    type: 'user',
                    name: '小明',
                    latestMessage: '优先处理日构建事务',
                    time: 1721219858
                },
                {
                    key: 2,
                    id: 2,
                    type: 'user',
                    name: '小笨',
                    latestMessage: '优先处理日构建事务',
                    time: 1721219858
                },
                {
                    key: 3,
                    id: 1,
                    type: 'group',
                    name: '小明',
                    latestMessage: '优先处理日构建事务',
                    time: 1721219858
                },
                {
                    key: 4,
                    id: 2,
                    type: 'group',
                    name: '小笨',
                    latestMessage: '优先处理日构建事务',
                    time: 1721219858
                }
            ]
        }
    },
    computed: {
        filterlist() {
            return this.messagelist.filter(item => item.name.includes(this.filterInput))
        }
    },
    methods: {
        timestrapToDate(timestrap) {
            let date = new Date(timestrap * 1000);
            let Y = date.getFullYear() + '-';
            let M = (date.getMonth() + 1 < 10 ? '0' + (date.getMonth() + 1) : date.getMonth() + 1) + '-';
            let D = date.getDate();
            return Y + M + D;
        },
        timestrapToTime(timestrap) {
            let date = new Date(timestrap * 1000);
            let h = date.getHours() + ':';
            let m = date.getMinutes();
            return h + m;
        },
        handleSelect(key) {
            this.controlInfo.selectId = key
        },
        openAddList() {
            this.controlInfo.showAddList = true;
        }
    },
}
</script>


<style lang="scss" scoped>
.message-container {
    width: 100%;
    height: 100%;
    border-right: 1px solid var(--el-border-color-extra-light);
    border-left: 1px solid var(--el-border-color-extra-light);

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
            height: 27px;
        }

        .search-add-friend {
            width: 15%;
            height: 100%;
            display: flex;
            justify-content: right;
            align-items: center;
            padding: 0;
            position: relative;
            overflow: visible;

            :deep(svg) {
                width: 70%;
                height: 70%;
                color: var(--color-base);
            }

            :deep(svg:hover) {
                color: var(--color-light-2)
            }

            .add-list {
                width: 120px;
                position: absolute;
                left: 10px;
                top: calc(100% - 15px);
                z-index: 2;
                border-radius: 5px;
                display: flex;
                flex-direction: column;
                background-color: var(--el-bg-color);
                user-select: none;
                box-shadow: 0 0 2px var(--el-border-color-light);

                .list-item {
                    padding: 5px;
                    display: flex;

                    .list-item-content {
                        width: 100%;
                        height: 20px;
                        padding: 5px;
                        display: flex;
                        justify-content: left;
                        align-items: center;
                        font-size: 12px;
                        border-radius: 5px;
                        background-color: var(--el-bg-color);

                        .list-item-icon {
                            width: 20px;
                            height: 20px;
                            display: flex;
                            justify-content: center;
                            align-items: center;
                            margin-right: 10px;

                            :deep(svg) {
                                width: 100%;
                                height: 100%;
                                color: var(--el-text-color-primary);
                            }
                        }
                    }

                    .list-item-content:hover {
                        background-color: var(--el-color-info-light-9);
                    }
                }

            }
        }

    }

    .messagelist-container {
        padding: 0;
        padding-right: 0;

        .messagelist-container-inner {
            padding-right: 0px;

            .message {
                width: 100%;
                height: 60px;
                display: flex;
                align-items: center;
                user-select: none;
                padding-top: 8px;
                padding-bottom: 8px;

                .message-avatar {
                    width: 60px;
                    height: 60px;
                    padding-left: 10px;
                    display: flex;
                    justify-content: center;
                    align-items: center;
                }

                .message-info {
                    flex: 1;
                    width: 0;
                    height: 100%;
                    display: flex;
                    flex-direction: column;
                    justify-content: center;

                    .message-name {
                        width: 100%;
                        height: 35%;
                        display: flex;
                        justify-content: center;
                        align-items: center;

                        .name-content {
                            flex: 1;
                            height: 100%;
                            display: flex;
                            justify-content: left;
                            align-items: center;
                            line-height: 100%;
                            font-size: 14px;
                        }
                    }

                    .message-latest-message {
                        width: 100%;
                        height: 30%;
                        display: flex;
                        justify-content: left;
                        align-items: center;

                        .message-latest-message-item {
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
                    padding-right: 10px;
                    color: var(--el-color-info);
                    font-size: 11px;
                    display: flex;
                    flex-direction: column;
                    justify-content: center;
                    align-items: center;
                }
            }

            .message:hover {
                background-color: var(--el-color-info-light-9);
            }

            .message.selected {
                background-color: var(--el-color-info-light-8);
            }
        }
    }

}
</style>
