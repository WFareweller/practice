<template>
  <table class="table table-bordered table-striped">
  <!-- 标题区域 -->
  <thead>
      <tr>
          <slot name="header"></slot>
      </tr>
  </thead>
  <!-- 内容主题区域 -->
  <tbody>
      <tr v-for="(item, index) in data" :key="item.id">
          <slot name="body" :row="item" :index="index"></slot>
      </tr>
  </tbody>
  </table>
</template>

<script>
export default {
    name:'MyTable',
    props:{
        //表格的数据源
        data:{
            type: Array,
            required: true,
            default:[],
        }
    }
}
</script>

<style lang='less' scoped>

</style>