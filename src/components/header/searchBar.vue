<template>
  <div class="search-panel">
    <el-row class="m-header-searchbar">
      <el-col :span="3" class="left">
        <img
          src="//s0.meituan.net/bs/fe-web-meituan/e5eeaef/img/logo.png"
          alt="美团"
        />
      </el-col>
      <el-col :span="15" class="center">
        <div class="wrapper">
          <el-input
            placeholder="搜索商家或地点"
            v-model="searchWord"
            @focus="inputFocus"
            @blur="inputBlur"
            clearable
          ></el-input>
          <el-button type="primary">
            <i class="el-icon-search"></i>
          </el-button>
          <dl class="hotPlace" v-if="isHotPalce">
            <dt>热门搜索</dt>
            <!-- <dd><router-link to="'/'">故宫博物院</router-link></dd>
            <dd><router-link to="'/'">北京欢乐谷</router-link></dd>
            <dd><router-link to="'/'">故宫珍宝馆</router-link></dd>
            <dd><router-link to="'/'">尚隐·泉都市生活馆</router-link></dd>
            <dd><router-link to="'/'">八达岭长城</router-link></dd> -->
            <dd v-for="(item, index) in hotPlace" :key="index">
              <router-link :to="{ name: 'goods', params: { name: item } }">{{
                item.name
              }}</router-link>
            </dd>
          </dl>
          <dl class="searchList" v-if="isSearchList">
            <!-- <dd><router-link to="'/'">火锅</router-link></dd>
            <dd><router-link to="'/'">火锅自助</router-link></dd>
            <dd><router-link to="'/'">重庆</router-link></dd> -->
            <dd v-for="(item, index) in searchList" :key="index">
              <router-link :to="{ name: 'goods', params: { name: item } }">{{
                item.name
              }}</router-link>
            </dd>
          </dl>
        </div>
        <p class="suggest">
          <router-link to="'/'">故宫博物院</router-link
          ><router-link to="'/'">北京欢乐谷</router-link
          ><router-link to="'/'">故宫珍宝馆</router-link
          ><router-link to="'/'">尚隐·泉都市生活馆</router-link
          ><router-link to="'/'">八达岭长城</router-link
          ><router-link to="'/'">北京连升商务酒店</router-link>
        </p>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  data () {
    return {
      searchWord: '',
      isFocus: false,
      hotPlace: [],
      searchList: []
    }
  },
  computed: {
    isHotPalce () {
      return this.isFocus && !this.searchWord
    },
    isSearchList () {
      return this.isFocus && this.searchWord
    }
  },
  methods: {
    inputFocus () {
      this.isFocus = true
    },
    inputBlur () {
      this.isFocus = false
    }
  }
}
</script>

<style lang="scss">
@import "@/assets/css/public/header/search.scss";
</style>
