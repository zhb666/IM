<!-- 最左边的选择框 -->
<template>
  <div>
    <div class="mycard">
      <header>
        <img :src="user.img" class="avatar" />
      </header>
      <footer>
        <i class="icon iconfont icon-more"></i>
      </footer>
    </div>

    <search></search>

    <div class="navbar" @click="clearSearch">
      <router-link to="/chat" class="icon iconfont icon-msg"></router-link>
      <router-link to="/friend" class="icon iconfont icon-friend"></router-link>
      <!-- <router-link to="/my" class="icon iconfont icon-collection"></router-link> -->
    </div>
  </div>
</template>

<script>
import search from "../../components/search/search";
import { mapState } from "vuex";
export default {
  components: {
    search
  },
  computed: {
    ...mapState(["user"])
  },
  methods: {
    clearSearch() {
      this.$store.dispatch("search", "");
    }
  }
};
</script>

<style lang="stylus" scoped>
@import '../../assets/fonts/iconfont.css';

.mycard {
  position: relative;
  width: 100%;
  height: 72px;
  background :url('../../../static/img/head_img.png') no-repeat;

  .avatar {
    width: 48px;
    height: 48px;
    margin: 12px 12px 0 12px;
    border-radius: 50%;
  }
}

footer {
  position: absolute;
  bottom: 24px;
  width: 100%;
  text-align: center;
  right :-104px;
}

.navbar {
    width: 100%;
    height:60px;
    background :#fff;
    text-align :center
    a{
      width :50%;
      display :block;
      float :left;
    }
  }

  .icon {
    display: inline-block;
    font-size: 26px;
    margin-top: 20px;
    padding: 0 16px;
    box-sizing: border-box;
    color: #ccc;
    opacity: 0.8;
    cursor: pointer;

    &.active {
      color: rgb(0, 220, 65);
    }

    &:hover {
      opacity: 1;
    }
  }

  .icon-msg, .icon-more {
    font-size: 22px;
  }

  .icon-msg {
    padding: 0 19px;
    border-right:1px solid #ccc
  }
  .icon-more{
    color :#fff;
  }
</style>
