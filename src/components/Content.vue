<template>
  <el-container>
    <el-main class="content-layout">
      <Title />
      <Package />
      <PackageDetail />
    </el-main>
  </el-container>
</template>

<script>
  import Title from "./Content/Title";
  import Package from "./Content/Package";
  import PackageDetail from "./Content/Package-Detail";

  export default {
    name: 'Content',
    components: {
      Title,
      Package,
      PackageDetail
    }
  };
</script>

<style lang="scss">
  .content-layout {
    background-color: #efefef;
    padding: 20px;
  }
</style>

