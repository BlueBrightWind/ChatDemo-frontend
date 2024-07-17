<template>
    <el-container class="friend-container">
        <el-header class="search-container">
            <el-container style="width: 100%; height: 100%;">
                <el-aside class="search-input">
                    <el-input v-model="filterInput" placeholder="搜索" :prefix-icon="Search" />
                </el-aside>
                <el-main class="search-add-friend">
                    <CirclePlusFilled />
                    <div class="add-friend-list">
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
        <el-main class="friendlist-container">
            <el-scrollbar class="friendlist-container-inner">
                <div class="list-container" :class="{ show: controlInfo.user.show }">
                    <div class="list-title" @click.stop="handleToggleUserList">
                        <el-icon class="list-title-icon">
                            <ArrowRight />
                        </el-icon>
                        <div class="list-title-content">我的好友</div>
                    </div>
                    <div v-show="controlInfo.user.show" class="list-content">
                        <!-- 示例开始 -->
                        <!-- <div class="user selected online">
                            <div class="user-avatar">
                                <el-avatar
                                    style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小笨</el-avatar>
                            </div>
                            <div class="user-info">
                                <div class="user-name">
                                    <div class="online-status"></div>
                                    <div class="name-content">
                                        <div class="name-content-item">
                                            小笨
                                        </div>
                                    </div>
                                </div>
                                <div class="user-desc">
                                    <span class="user-desc-item">优先处理日构建事务</span>
                                </div>
                            </div>
                        </div>
                        <div class="user offline">
                            <div class="user-avatar">
                                <el-avatar
                                    style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小笨</el-avatar>
                            </div>
                            <div class="user-info">
                                <div class="user-name">
                                    <div class="online-status"></div>
                                    <div class="name-content">
                                        <div class="name-content-item">
                                            小笨
                                        </div>
                                    </div>
                                </div>
                                <div class="user-desc">
                                    <span class="user-desc-item">优先处理日构建事务</span>
                                </div>
                            </div>
                        </div> -->
                        <!-- 示例结束 -->
                        <!-- 测试开始 -->
                        <div v-for="user, index in userlist" class="user"
                            :class="{ online: user.online, offline: !user.online, selected: controlInfo.selectId == user.key }"
                            @click="handleSelect(user.key)">
                            <div class="user-avatar">
                                <el-avatar style="width: 75%; height: 75%; background-color: var(--color-dark-2);">{{
                                    user.name.substring(user.name.length - 2) }}</el-avatar>
                            </div>
                            <div class="user-info">
                                <div class="user-name">
                                    <div class="online-status"></div>
                                    <div class="name-content">
                                        <div class="name-content-item">
                                            {{ user.name }}
                                        </div>
                                    </div>
                                </div>
                                <div class="user-desc">
                                    <span class="user-desc-item">{{ user.desc }}</span>
                                </div>
                            </div>
                        </div>
                        <!-- 测试结束 -->
                    </div>
                </div>
                <div class="list-container" :class="{ show: controlInfo.group.show }">
                    <div class="list-title" @click.stop="handleToggleGroupList">
                        <el-icon class="list-title-icon">
                            <ArrowRight />
                        </el-icon>
                        <div class="list-title-content">我的群聊</div>
                    </div>
                    <div v-show="controlInfo.group.show" class="list-content">
                        <!-- 示例开始 -->
                        <!-- <div class="group selected">
                            <div class="group-avatar">
                                <el-avatar
                                    style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小明</el-avatar>
                            </div>
                            <div class="group-info">
                                <div class="group-name">
                                    <div class="name-content">
                                        <div class="name-content-item">小明</div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="group">
                            <div class="group-avatar">
                                <el-avatar
                                    style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小笨</el-avatar>
                            </div>
                            <div class="group-info">
                                <div class="group-name">
                                    <div class="name-content">
                                        <div class="name-content-item">小笨</div>
                                    </div>
                                </div>
                            </div>
                        </div> -->
                        <!-- 示例结束 -->
                        <!-- 测试开始 -->
                        <div v-for="group, index in grouplist" class="group"
                            :class="{ selected: controlInfo.selectId == group.key }" @click="handleSelect(group.key)">
                            <div class="group-avatar">
                                <el-avatar style="width: 75%; height: 75%; background-color: var(--color-dark-2);">{{
                                    group.name.substring(group.name.length - 2) }}</el-avatar>
                            </div>
                            <div class="group-info">
                                <div class="group-name">
                                    <div class="name-content">
                                        <div class="name-content-item">{{ group.name }}</div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <!-- 测试结束 -->
                    </div>
                </div>
            </el-scrollbar>
        </el-main>
    </el-container>
</template>

<script setup>
import { Search, ArrowRight } from '@element-plus/icons-vue'
import { CirclePlusFilled, User, ChatDotSquare } from '@element-plus/icons-vue'
</script>

<script>
export default {
    name: 'FriendList',
    data() {
        return {
            filterInput: '',
            controlInfo: {
                user: {
                    show: false,
                },
                group: {
                    show: false,
                },
                selectId: 0
            },
            frientlist: [
                {
                    key: 1,
                    id: 1,
                    type: 'user',
                    name: '小明',
                    desc: '优先处理日构建事务',
                    online: true
                },
                {
                    key: 2,
                    id: 2,
                    type: 'user',
                    name: '小笨',
                    desc: '优先处理日构建事务',
                    online: true
                },
                {
                    key: 3,
                    id: 1,
                    type: 'group',
                    name: '小明'
                },
                {
                    key: 4,
                    id: 2,
                    type: 'group',
                    name: '小笨'
                }
            ]
        }
    },
    computed: {
        filterlist() {
            return this.frientlist.filter(item => item.name.includes(this.filterInput))
        },
        userlist() {
            return this.filterlist.filter(item => item.type === 'user')
        },
        grouplist() {
            return this.filterlist.filter(item => item.type === 'group')
        }
    },
    methods: {
        handleToggleUserList() {
            this.controlInfo.user.show = !this.controlInfo.user.show;
        },
        handleToggleGroupList() {
            this.controlInfo.group.show = !this.controlInfo.group.show;
        },
        handleSelect(key) {
            this.controlInfo.selectId = key
        },

    }

}
</script>


<style lang="scss" scoped>
.friend-container {
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

            .add-friend-list {
                width: 120px;
                position: absolute;
                left: 10px;
                top: calc(100% - 15px);
                z-index: 3;
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

    .friendlist-container {
        padding: 0;
        padding-right: 0;

        .friendlist-container-inner {
            padding-right: 0px;

            :deep(.el-scrollbar__bar) {
                z-index: 2;
            }

            .list-container {

                .list-title {
                    width: 100%;
                    height: 40px;
                    display: flex;
                    align-items: center;
                    user-select: none;
                    position: sticky;
                    top: 0;
                    z-index: 2;
                    background-color: var(--el-bg-color);

                    .list-title-icon {
                        margin-left: 10px;
                        margin-right: 10px;
                        font-size: 12px;
                        transition-duration: 0.25s;
                    }

                    .list-title-content {
                        width: 100%;
                        height: 100%;
                        display: flex;
                        justify-content: left;
                        align-items: center;
                        font-size: 14px;
                    }


                }

                .list-content {
                    transition-duration: 0.25s;
                }
            }

            .list-container.show {

                .list-title-icon {
                    transform: rotate(90deg);
                }
            }

            .user {
                width: 100%;
                height: 60px;
                display: flex;
                align-items: center;
                user-select: none;
                padding-top: 8px;
                padding-bottom: 8px;

                .user-avatar {
                    width: 60px;
                    height: 60px;
                    padding-left: 10px;
                    display: flex;
                    justify-content: center;
                    align-items: center;
                }

                .user-info {
                    flex: 1;
                    width: 0;
                    height: 100%;
                    display: flex;
                    flex-direction: column;
                    justify-content: center;
                    padding-right: 10px;

                    .user-name {
                        width: 100%;
                        height: 35%;
                        display: flex;
                        justify-content: center;
                        align-items: center;

                        .online-status {
                            width: 10px;
                            height: 10px;
                            border-radius: 50%;
                            margin-right: 5px;
                            background-color: var(--el-color-success);
                        }

                        .name-content {
                            flex: 1;
                            width: 0;
                            height: 100%;
                            display: flex;
                            justify-content: left;
                            align-items: center;

                            .name-content-item {
                                width: 100%;
                                height: 100%;
                                font-size: 14px;
                                white-space: nowrap;
                                overflow: hidden;
                                text-overflow: ellipsis;
                            }
                        }
                    }

                    .user-desc {
                        width: 100%;
                        height: 30%;
                        display: flex;
                        justify-content: left;
                        align-items: center;

                        .user-desc-item {
                            white-space: nowrap;
                            overflow: hidden;
                            text-overflow: ellipsis;
                            font-size: 11px;
                            color: var(--el-color-info);
                        }
                    }
                }
            }

            .user:hover {
                background-color: var(--el-color-info-light-9);
            }

            .user.selected {
                background-color: var(--el-color-info-light-8);
            }

            .user.online {
                filter: grayscale(0);
            }

            .user.offline {
                filter: grayscale(1);
            }

            .group {
                width: 100%;
                height: 60px;
                display: flex;
                align-items: center;
                user-select: none;
                padding-top: 8px;
                padding-bottom: 8px;

                .group-avatar {
                    width: 60px;
                    height: 60px;
                    padding-left: 10px;
                    display: flex;
                    justify-content: center;
                    align-items: center;
                }

                .group-info {
                    flex: 1;
                    width: 0;
                    height: 100%;
                    display: flex;
                    flex-direction: column;
                    justify-content: center;

                    .group-name {
                        width: 100%;
                        height: 35%;
                        display: flex;
                        justify-content: center;
                        align-items: center;

                        .name-content {
                            flex: 1;
                            width: 0;
                            height: 100%;
                            display: flex;
                            justify-content: left;
                            align-items: center;
                            line-height: 100%;
                            font-size: 14px;

                            .name-content-item {
                                width: 100%;
                                height: 100%;
                                font-size: 14px;
                                white-space: nowrap;
                                overflow: hidden;
                                text-overflow: ellipsis;
                            }
                        }
                    }
                }
            }

            .group:hover {
                background-color: var(--el-color-info-light-9);
            }

            .group.selected {
                background-color: var(--el-color-info-light-8);
            }
        }
    }

}
</style>
