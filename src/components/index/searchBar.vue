<template>
  <div class="search-bar">
    <div class="search-icon">
      <span class="icon-mi">
        <i class="iconfont">&#xe605;</i>
      </span>
    </div>
    <div class="search-ipt">
      <input type="text" v-on:focus="searchShow" />
    </div>
    <div class="search-pic">
      <span class="icon-search">
        <i class="iconfont">&#xe606;</i>
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'searchBar',
  data () {
    return {
    }
  },
  methods:{
    searchShow:function(){
      this.$router.push({ path: '/search' })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
.search-bar{
  width: 100%;
  height: 40px;
  position: fixed;
  top: 0px;
  left: 0px;
  background: #f87300;
  z-index: 99;
  .search-icon{
    width:15%;
    color:#ffffff;
    float:left;
    .icon-mi{
      width:20px;
      height:20px;
      display:inline-block;
      padding-top:7px;
      i{
        font-size: 24px;
      }
    }
  }
  .search-ipt{
    width:70%;
    float:left;
    input{
      width:96%;
      height:30px;
      line-height:30px;
      border:0;
      outline:0;
      background:#ffffff;
      padding-left:2%;
      margin:5px auto;
      border-radius:5px;
    }
  }
  .search-pic{
    width:15%;
    float:left;
    .icon-search{
      width:20px;
      height:20px;
      display:inline-block;
      padding-top:10px;
      i{
        color:#ffffff;
      }
    }
  }
}
</style>
