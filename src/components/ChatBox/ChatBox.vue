<template>
    <div class="chatbox">
        <!-- <el-container>
            <el-aside style="overflow: visible;">
                <FriendList />
            </el-aside>
            <el-main style="padding: 0;">
                <ChatContainer />
            </el-main>
        </el-container> -->
        <AddFriend />


    </div>
</template>

<script>
import FriendList from "./FriendList/FriendList.vue";
import ChatContainer from "./UserChat/GroupChat.vue";
import AddFriend from "./AddFriend/AddFriend.vue";

export default {
    name: 'ChatBox',
    components: {
        FriendList,
        ChatContainer,
        AddFriend
    }
}
</script>

<style lang="scss" scoped>
.chatbox {
    width: 1400px;
    height: 700px;
    box-shadow: 0 0 5px var(--el-color-info-light-3);
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    display: flex;
    border-radius: 5px;
}
</style>