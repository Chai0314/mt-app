<template>
  <div class="m-menu">
    <div class="nav" @mouseleave="mouseLeave">
      <dl>
        <dt>全部分类</dt>
        <dd
          v-for="(item, index) in menuList"
          :key="index"
          @mouseenter="mouseEnter(item.children)"
        >
          <i :class="item.icon"></i>
          {{ item.title }}
          <span class="arrow"></span>
        </dd>
      </dl>
    </div>
    <div
      v-if="curDetail"
      class="detail"
      @mouseenter="detailEnter"
      @mouseleave="detailLeave"
    >
      <template v-for="(item, index) in curDetail">
        <h4 :key="index">{{ item.title }}</h4>
        <span v-for="(v, i) in item.children" :key="i">{{ v }}</span>
      </template>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      curDetail: null,
      menuList: [
        {
          title: "美食",
          icon: "food",
          children: [
            {
              title: "美食",
              children: ["代金券", "甜点饮品", "火锅自助餐", "小吃快餐"],
            },
          ],
        },
        {
          title: "外卖",
          icon: "takeout",
          children: [
            {
              title: "外卖",
              children: ["美团外卖"],
            },
          ],
        },
        {
          title: "酒店",
          icon: "hotel",
          children: [
            {
              title: "酒酒店星级店",
              children: ["经济型舒适", "/三星高档", "/四星豪华", "/五星"],
            },
          ],
        },
      ],
    };
  },
  methods: {
    mouseEnter(item) {
      if (item) this.curDetail = item;
    },
    mouseLeave() {
      var slef = this;
      this.timer = setTimeout(function () {
        slef.curDetail = null;
      }, 0);
    },
    detailEnter() {
      clearTimeout(this.timer);
    },
    detailLeave() {
      this.curDetail = null;
    },
  },
};
</script>

<style>
</style>
