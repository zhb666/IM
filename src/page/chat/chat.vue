<template>
  <div class="content">
    <div class="msglist">
      <mycard></mycard>
      <!-- <search></search> -->
      <chatlist></chatlist>
    </div>
    <div class="chatbox">
      <message></message>
      <v-text></v-text>
    </div>
  </div>
</template>

<script>
import mycard from "../../components/mycard/mycard";
import search from "../../components/search/search";
import chatlist from "../../components/chatlist/chatlist";
import message from "../../components/message/message";
import vText from "../../components/text/text";
export default {
  components: {
    mycard,
    search,
    chatlist,
    message,
    vText
  }
};
</script>

<style lang="stylus" scoped>
.content {
  display: flex;
  width: 1024px;

  .sidebar {
    width: 280px;
    height: 72px;
    background: #2b2c2f;
  }

  .msglist {
    width: 280px;
    background: #fff;
  }

  .chatbox {
    flex: 1;
  }
}
</style>
