<template>
  <div class="m-header">
      <el-row>
          <topBar/>
      </el-row>
      <el-row>
          <searchBarVue/>
      </el-row>
  </div>
</template>

<script>
import topBar from './topBar.vue'
import searchBarVue from './searchBar.vue'
export default {
  components: {
    topBar,
    searchBarVue
  }
}
</script>

<style>

</style>
