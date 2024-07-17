<template>
    <div class="chatbox">
        <el-container>
            <el-aside style="overflow: visible; width: 70px;">
                <SideBar />
            </el-aside>
            <el-aside style="overflow: visible; width: 250px;">
                <FriendList />
            </el-aside>
            <el-main style="padding: 0;">
                <!-- <UserChatContainer /> -->
                <GroupChatContainer />
                <!-- <UserAddNotice /> -->
                <!-- <GroupAddNotice /> -->
            </el-main>
        </el-container>
        <!-- <AddFriend /> -->


    </div>
</template>

<script>
import FriendList from "./FriendList/FriendList.vue";
import UserChatContainer from "./UserChat/UserChat.vue";
import GroupChatContainer from "./UserChat/GroupChat.vue";
import AddFriend from "./AddFriend/AddFriend.vue";
import UserAddNotice from "./AddNotice/UserAddNotice.vue";
import GroupAddNotice from "./AddNotice/GroupAddNotice.vue";
import SideBar from "./SideBar/SideBar.vue";


export default {
    name: 'ChatBox',
    components: {
        SideBar,
        FriendList,
        UserChatContainer,
        GroupChatContainer,
        AddFriend,
        UserAddNotice,
        GroupAddNotice
    }
}
</script>

<style lang="scss" scoped>
.chatbox {
    width: 1200px;
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