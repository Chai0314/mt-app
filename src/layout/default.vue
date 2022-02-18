<template>
  <div class="layout-default">
    <el-container>
      <el-header height="">
        <myHeader />
      </el-header>
      <el-main>
        <router-view></router-view>
      </el-main>
      <el-footer height="">
        <myFooter />
      </el-footer >
    </el-container>
  </div>
</template>

<script>
import myHeader from '@/components/header'
import myFooter from '@/components/footer'
export default {
  components: {
    myHeader,
    myFooter
  }
}
</script>

<style lang="scss">
@import "@/assets/css/public/layout.scss";
</style>
