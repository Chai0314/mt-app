<template>
  <div class="m-nav">
    <ul class="nav">
      <li class="list">
        <router-link to="'/my-app">我的美团</router-link>
        <dl>
          <dd>我的订单</dd>
          <dd>我的收藏</dd>
          <dd>抵用券</dd>
          <dd>账户设置</dd>
        </dl>
      </li>
      <li>
        <router-link to="'/ipone-app">手机APP</router-link>
      </li>
      <li class="list">
        <router-link to="'/my-app1">商家中心</router-link>
        <dl>
          <dd>登录商家中心</dd>
          <dd>美团智能收银</dd>
          <dd>我想合作</dd>
          <dd>账户设置</dd>
        </dl>
      </li>
      <li class="list">
        <router-link to="'/my-app2">网站导航</router-link>
        <div class="subContainer">
          <dl class="hotel">
            <dt>酒店旅游</dt>
            <dd>我的订单</dd>
            <dd>我的收藏</dd>
            <dd>抵用券</dd>
            <dd>账户设置</dd>
          </dl>
          <dl class="food">
            <dt>吃美食</dt>
            <dd>我的订单</dd>
            <dd>我的收藏</dd>
            <dd>抵用券</dd>
            <dd>账户设置</dd>
          </dl>
          <dl class="movie">
            <dt>看电影</dt>
            <dd>我的订单</dd>
            <dd>我的收藏</dd>
            <dd>抵用券</dd>
            <dd>账户设置</dd>
          </dl>
          <dl class="app">
            <dt>手机应用</dt>
            <dd>
              <a href="#">
                <img
                  class="appicon"
                  src="//s0.meituan.net/bs/fe-web-meituan/e5eeaef/img/appicons/meituan.png"
                  title="美团app"
                  alt="美团app"
                />
              </a>
            </dd>
                        <dd>
              <a href="#">
                <img
                  class="appicon"
                  src="//s0.meituan.net/bs/fe-web-meituan/e5eeaef/img/appicons/meituan.png"
                  title="美团app"
                  alt="美团app"
                />
              </a>
            </dd>
                        <dd>
              <a href="#">
                <img
                  class="appicon"
                  src="//s0.meituan.net/bs/fe-web-meituan/e5eeaef/img/appicons/meituan.png"
                  title="美团app"
                  alt="美团app"
                />
              </a>
            </dd>
          </dl>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {}
</script>

<style>
</style>
