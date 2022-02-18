<template>
  <div class="page-index">
    <el-row>
        <el-col :span="5">
            <my-menu />
        </el-col>
        <el-col :span="19">
            <my-life />
        </el-col>
    </el-row>
    <el-row>
         <el-col :span="24">
             container
        </el-col>
    </el-row>
  </div>
</template>

<script>
import myMenu from '@/components/index/menu.vue'
import myLife from '@/components/index/life.vue'
export default {
  components: {
    myMenu,
    myLife
  }
}
</script>

<style lang="scss">
    @import "@/assets/css/index/index.scss"
</style>