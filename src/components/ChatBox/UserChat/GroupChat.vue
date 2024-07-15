<template>
    <el-container class="chat-container">
        <el-header class="chat-title">
            <el-button class="return-last">
                <el-icon>
                    <Back />
                </el-icon>
            </el-button>
            <div class="friend-avatar">
                <el-avatar style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小明</el-avatar>
            </div>
            <div class="friend-info">
                <div class="name-content">小明</div>
                <div class="desc-content">abcabcabc</div>
            </div>
        </el-header>
        <el-main class="chat-content">
            <el-container style="width: 100%; height: 100%;">
                <el-main class="chat-content-item">
                    <el-scrollbar class="chat-content-item-inner">
                        <!-- 消息体开始 -->
                        <el-container style="width: 100%;">
                            <el-header class="content-message-time show">2024/07/10 14:53</el-header>
                            <el-main class="content-item">
                                <el-container style="width: 100%;">
                                    <el-aside class="content-item-avatar">
                                        <el-avatar
                                            style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小明</el-avatar>
                                    </el-aside>
                                    <el-main class="content-item-message">
                                        <div class="message-item">
                                            哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈
                                        </div>
                                    </el-main>
                                    <el-aside class="content-item-avatar">
                                        <!-- <el-avatar style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小红</el-avatar> -->
                                    </el-aside>
                                </el-container>
                            </el-main>
                        </el-container>
                        <!-- 消息体结束 -->
                        <!-- 消息体开始 -->
                        <el-container style="width: 100%;">
                            <el-header class="content-message-time">2024/07/10 14:53</el-header>
                            <el-main class="content-item">
                                <el-container style="width: 100%;">
                                    <el-aside class="content-item-avatar">
                                        <!-- <el-avatar style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小明</el-avatar> -->
                                    </el-aside>
                                    <el-main class="content-item-message message-right">
                                        <div class="message-item">
                                            哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈
                                        </div>
                                    </el-main>
                                    <el-aside class="content-item-avatar">
                                        <el-avatar
                                            style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小红</el-avatar>
                                    </el-aside>
                                </el-container>
                            </el-main>
                        </el-container>
                        <!-- 消息体结束 -->
                        <!-- 测试开始 -->
                        <el-container style="width: 100%;">
                            <el-header class="content-message-time">2024/07/10 14:53</el-header>
                            <el-main class="content-item">
                                <el-container style="width: 100%;">
                                    <el-aside class="content-item-avatar">
                                        <el-avatar
                                            style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小明</el-avatar>
                                    </el-aside>
                                    <el-main class="content-item-message">
                                        <div class="message-item">
                                            哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈
                                        </div>
                                    </el-main>
                                    <el-aside class="content-item-avatar">
                                        <!-- <el-avatar style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小红</el-avatar> -->
                                    </el-aside>
                                </el-container>
                            </el-main>
                        </el-container>
                        <el-container style="width: 100%;">
                            <el-header class="content-message-time show">2024/07/10 14:53</el-header>
                            <el-main class="content-item">
                                <el-container style="width: 100%;">
                                    <el-aside class="content-item-avatar">
                                        <!-- <el-avatar style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小明</el-avatar> -->
                                    </el-aside>
                                    <el-main class="content-item-message message-right">
                                        <div class="message-item">
                                            哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈
                                        </div>
                                    </el-main>
                                    <el-aside class="content-item-avatar">
                                        <el-avatar
                                            style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小红</el-avatar>
                                    </el-aside>
                                </el-container>
                            </el-main>
                        </el-container>
                        <el-container style="width: 100%;">
                            <el-header class="content-message-time">2024/07/10 14:53</el-header>
                            <el-main class="content-item">
                                <el-container style="width: 100%;">
                                    <el-aside class="content-item-avatar">
                                        <el-avatar
                                            style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小明</el-avatar>
                                    </el-aside>
                                    <el-main class="content-item-message">
                                        <div class="message-item">
                                            哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈
                                        </div>
                                    </el-main>
                                    <el-aside class="content-item-avatar">
                                        <!-- <el-avatar style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小红</el-avatar> -->
                                    </el-aside>
                                </el-container>
                            </el-main>
                        </el-container>
                        <el-container style="width: 100%;">
                            <el-header class="content-message-time">2024/07/10 14:53</el-header>
                            <el-main class="content-item">
                                <el-container style="width: 100%;">
                                    <el-aside class="content-item-avatar">
                                        <!-- <el-avatar style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小明</el-avatar> -->
                                    </el-aside>
                                    <el-main class="content-item-message message-right">
                                        <div class="message-item">
                                            哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈
                                        </div>
                                    </el-main>
                                    <el-aside class="content-item-avatar">
                                        <el-avatar
                                            style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小红</el-avatar>
                                    </el-aside>
                                </el-container>
                            </el-main>
                        </el-container>
                        <el-container style="width: 100%;">
                            <el-header class="content-message-time">2024/07/10 14:53</el-header>
                            <el-main class="content-item">
                                <el-container style="width: 100%;">
                                    <el-aside class="content-item-avatar">
                                        <el-avatar
                                            style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小明</el-avatar>
                                    </el-aside>
                                    <el-main class="content-item-message">
                                        <div class="message-item">
                                            哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈
                                        </div>
                                    </el-main>
                                    <el-aside class="content-item-avatar">
                                        <!-- <el-avatar style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小红</el-avatar> -->
                                    </el-aside>
                                </el-container>
                            </el-main>
                        </el-container>
                        <el-container style="width: 100%;">
                            <el-header class="content-message-time">2024/07/10 14:53</el-header>
                            <el-main class="content-item">
                                <el-container style="width: 100%;">
                                    <el-aside class="content-item-avatar">
                                        <!-- <el-avatar style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小明</el-avatar> -->
                                    </el-aside>
                                    <el-main class="content-item-message message-right">
                                        <div class="message-item">
                                            哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈
                                        </div>
                                    </el-main>
                                    <el-aside class="content-item-avatar">
                                        <el-avatar
                                            style="width: 75%; height: 75%; background-color: var(--color-dark-2);">小红</el-avatar>
                                    </el-aside>
                                </el-container>
                            </el-main>
                        </el-container>
                        <!-- 测试结束 -->
                    </el-scrollbar>
                </el-main>
                <el-aside class="chat-group-info">
                    <el-container style="width: 100%; height: 100%;">
                        <el-header class="chat-group-desc">
                            <div class="group-desc-title">群公告</div>
                            <div class="group-desc-content">
                                <el-scrollbar class="group-desc-content-inner">
                                    <div class="group-desc-content-item">
                                        1. 本群禁止任何形式的广告宣传，一经发现，立即踢出群聊。
                                        2. 本群禁止任何形式的广告宣传，一经发现，立即踢出群聊。
                                        3. 本群禁止任何形式的广告宣传，一经发现，立即踢出群聊。
                                        4. 本群禁止任何形式的广告宣传，一经发现，立即踢出群聊。
                                        5. 本群禁止任何形式的广告宣传，一经发现，立即踢出群聊。
                                        6. 本群禁止任何形式的广告宣传，一经发现，立即踢出群聊。
                                        aaaaaaaaaaaaaaaaabbbbbbbbbbbbbbbbbbcccccccccccccccccccccccccc
                                    </div>
                                </el-scrollbar>

                            </div>
                        </el-header>
                        <el-main class="chat-group-userlist">
                            <div class="group-userlist-title">群聊成员</div>
                            <div class="group-userlist-content">
                                <el-scrollbar class="group-userlist-content-inner">
                                    <!-- 群组成员信息开始 -->
                                    <div class="group-userlist-content-item">
                                        <el-avatar class="group-userlist-avatar-mini">明</el-avatar>
                                        <div class="group-userlist-username">小明</div>
                                    </div>
                                    <!-- 群组成员信息结束 -->
                                    <!-- 测试开始 -->
                                    <div class="group-userlist-content-item">
                                        <el-avatar class="group-userlist-avatar-mini">明</el-avatar>
                                        <div class="group-userlist-username">小明aaaaaaaaaaaaaaaaaaaaaaa</div>
                                    </div>
                                    <div class="group-userlist-content-item">
                                        <el-avatar class="group-userlist-avatar-mini">明</el-avatar>
                                        <div class="group-userlist-username">小明</div>
                                    </div>
                                    <div class="group-userlist-content-item">
                                        <el-avatar class="group-userlist-avatar-mini">明</el-avatar>
                                        <div class="group-userlist-username">小明</div>
                                    </div>
                                    <div class="group-userlist-content-item">
                                        <el-avatar class="group-userlist-avatar-mini">明</el-avatar>
                                        <div class="group-userlist-username">小明</div>
                                    </div>
                                    <div class="group-userlist-content-item">
                                        <el-avatar class="group-userlist-avatar-mini">明</el-avatar>
                                        <div class="group-userlist-username">小明</div>
                                    </div>
                                    <div class="group-userlist-content-item">
                                        <el-avatar class="group-userlist-avatar-mini">明</el-avatar>
                                        <div class="group-userlist-username">小明</div>
                                    </div>
                                    <div class="group-userlist-content-item">
                                        <el-avatar class="group-userlist-avatar-mini">明</el-avatar>
                                        <div class="group-userlist-username">小明</div>
                                    </div>
                                    <div class="group-userlist-content-item">
                                        <el-avatar class="group-userlist-avatar-mini">明</el-avatar>
                                        <div class="group-userlist-username">小明</div>
                                    </div>
                                    <div class="group-userlist-content-item">
                                        <el-avatar class="group-userlist-avatar-mini">明</el-avatar>
                                        <div class="group-userlist-username">小明</div>
                                    </div>
                                    <div class="group-userlist-content-item">
                                        <el-avatar class="group-userlist-avatar-mini">明</el-avatar>
                                        <div class="group-userlist-username">小明</div>
                                    </div>
                                    <!-- 测试结束 -->
                                </el-scrollbar>
                            </div>
                        </el-main>
                    </el-container>
                </el-aside>
            </el-container>
        </el-main>
        <el-footer class="chat-input">
            <div class="chat-input-box">
                <el-input class="inputbox" v-model="inputValue" maxlength="255" show-word-limit></el-input>
            </div>
            <div class="chat-input-button">
                <el-button class="function-button">
                    <el-icon>
                        <Sunrise />
                    </el-icon>
                </el-button>
                <el-button class="function-button">
                    <el-icon>
                        <Microphone />
                    </el-icon>
                </el-button>
                <el-button class="function-button">
                    <el-icon>
                        <Camera />
                    </el-icon>
                </el-button>
                <el-button class="function-button">
                    <el-icon>
                        <Monitor />
                    </el-icon>
                </el-button>
                <el-button class="function-button">
                    <el-icon>
                        <Folder />
                    </el-icon>
                </el-button>
                <el-button type="primary" style="outline: none;">发送</el-button>
            </div>
        </el-footer>
    </el-container>
</template>

<script setup>
import { Back, Microphone, Camera, Monitor, Folder, Sunrise } from '@element-plus/icons-vue'
</script>

<script>
export default {
    name: 'GroupChatContainer',
    data() {
        return {
            inputValue: ''
        }
    },
}
</script>

<style lang="scss" scoped>
.chat-container {
    height: 100%;
    display: flex;
    flex-direction: column;

    .chat-title {
        margin-top: 10px;
        display: flex;
        height: 65px;
        align-items: center;
        user-select: none;

        .return-last {
            width: 30px;
            height: 30px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 15px;
            outline: none;
            border: none;
        }

        .return-last:hover {
            background-color: var(--el-fill-color-light);
            color: inherit;
        }

        .friend-avatar {
            width: 65px;
            height: 65px;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .friend-info {
            display: flex;
            flex-direction: column;
            justify-content: center;
            margin: 10px;

            .name-content {
                font-size: 20px;
                font-weight: bold;
            }

            .desc-content {
                font-size: 12px;
                color: var(--el-color-info);
            }
        }
    }

    .chat-content {
        flex: 1;
        background-color: var(--el-bg-color-page);
        border-top: 1px solid var(--el-border-color-extra-light);
        border-bottom: 1px solid var(--el-border-color-extra-light);
        padding: 0;
        padding-left: 20px;

        .chat-content-item {
            padding: 0;

            .chat-content-item-inner {
                padding-right: 20px;

                .content-message-time {
                    display: none;
                    width: 100%;
                    height: 30px;
                    justify-content: center;
                    align-items: center;
                    font-size: 12px;
                    color: var(--el-color-info);
                    user-select: none;
                }

                .content-message-time.show {
                    display: flex;
                }

                .content-item {
                    width: 100%;
                    padding: 5px;

                    .content-item-avatar {
                        width: 40px;
                        height: 40px;
                        display: flex;
                        justify-content: center;
                        align-items: center;
                        user-select: none;

                        :deep(.el-avatar) {
                            font-size: 10px;
                        }
                    }

                    .content-item-message {
                        display: flex;
                        justify-content: left;
                        align-items: start;
                        padding-top: 0;
                        padding-bottom: 0;
                        padding-left: 10px;
                        padding-right: 10px;

                        .message-item {
                            padding-top: 5px;
                            padding-bottom: 5px;
                            padding-left: 10px;
                            padding-right: 10px;
                            border-radius: 5px;
                            line-height: 30px;
                            font-size: 14px;
                            text-align: left;
                            background-color: var(--el-fill-color-lighter);
                        }
                    }

                    .content-item-message.message-left {
                        justify-content: left;
                    }

                    .content-item-message.message-right {
                        justify-content: right;
                    }
                }
            }
        }

        .chat-group-info {
            border-left: 1px solid var(--el-border-color-light);
            width: 200px;
            display: flex;

            .chat-group-desc {
                padding: 10px;
                padding-right: 0;
                height: 200px;
                display: flex;
                flex-direction: column;
                border-bottom: 1px solid var(--el-border-color-light);

                .group-desc-title {
                    font-size: 14px;
                    font-weight: bold;
                    width: 100%;
                    height: 30px;
                    display: flex;
                    justify-content: left;
                    align-items: center;
                    user-select: none;
                }

                .group-desc-content {
                    flex: 1;
                    overflow: hidden;

                    .group-desc-content-inner {
                        padding-right: 10px;

                        .group-desc-content-item {
                            display: block;
                            width: 100%;
                            overflow: hidden;
                            font-size: 13px;
                            white-space: break-all;
                            color: var(--el-color-info);
                            user-select: none;
                        }
                    }
                }

            }

            .chat-group-userlist {
                flex: 1;
                padding: 10px;
                padding-right: 0;
                display: flex;
                flex-direction: column;

                .group-userlist-title {
                    font-size: 14px;
                    font-weight: bold;
                    width: 100%;
                    height: 30px;
                    display: flex;
                    justify-content: left;
                    align-items: center;
                    user-select: none;
                }

                .group-userlist-content {
                    flex: 1;
                    overflow: hidden;

                    .group-userlist-content-inner {
                        padding-right: 10px;

                        .group-userlist-content-item {
                            display: flex;
                            width: 100%;
                            height: 30px;
                            justify-content: left;
                            align-items: center;
                            user-select: none;

                            .group-userlist-avatar-mini {
                                font-size: 10px;
                                width: 20px;
                                height: 20px;
                                margin-right: 10px;
                                background-color: var(--color-dark-2);
                            }

                            .group-userlist-username {
                                flex: 1;
                                font-size: 13px;
                                color: var(--el-color-info);
                                white-space: nowrap;
                                overflow: hidden;
                                text-overflow: ellipsis;
                            }
                        }
                    }
                }


            }
        }
    }

    .chat-input {
        // background-color: var(--el-fill-color-light);
        height: 70px;
        padding-top: 10px;
        padding-bottom: 10px;
        display: flex;
        align-items: center;


        .chat-input-box {
            flex: 1;
            height: 100%;
            display: flex;
            align-items: center;
            position: relative;

            .inputbox {
                width: 100%;
                height: 80%;
            }

            .inputbox:deep(.el-input__wrapper) {
                border-radius: 999999px;
            }
        }

        .chat-input-button {
            display: flex;
            justify-content: center;
            align-items: center;
            padding-left: 10px;

            .function-button {
                border: 0;
                outline: none;
                background-color: transparent;
                font-size: 20px;
                width: 20px;
            }


        }
    }
}
</style>