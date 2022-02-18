<template>
  <div class="m-geo">
    <div class="position">
      <i class="el-icon-location"></i>
      杭州
      <router-link
        class="changeCity"
        :to="'/exChangeCity'"
      >
        切换城市
      </router-link>
      [
      <a href="#" v-for="(item, index) in nearCity" :key="index">{{
        item.name
      }}</a>
      ]
    </div>
    <div class="m-user">
        <router-link class="login" :to="'/login'">立即登录</router-link>
        <router-link class="register" :to="'/register'">注册</router-link>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      nearCity: [
        {
          id: 1,
          name: '北京',
          pinyin: 'beijing',
          acronym: 'bj',
          rank: 'S',
          firstChar: 'b'
        },
        {
          id: 10,
          name: '上海',
          pinyin: 'shanghai',
          acronym: 'sh',
          rank: 'S',
          firstChar: 's'
        }
      ]
    }
  }
}
</script>

<style>
</style>
