<template>
  <div class="content">
    <div class="friend-wrapper">
      <mycard></mycard>
      <!-- <search></search> -->
      <friendlist></friendlist>
    </div>
    <div class="friendinfo">
      <info></info>
    </div>
  </div>
</template>

<script>
import mycard from "../../components/mycard/mycard";
import search from "../../components/search/search";
import friendlist from "../../components/friendlist/friendlist";
import info from "../../components/info/info";
export default {
  components: {
    mycard,
    search,
    friendlist,
    info
  }
};
</script>

<style lang="stylus" scoped>
.content {
  display: flex;
  width: 1024px;

  .friend-wrapper {
    width: 280px;
    background: rgb(230, 230, 230);
  }

  .friendinfo {
    flex: 1;
  }
}
</style>