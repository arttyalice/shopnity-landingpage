<template>
  <el-container>
    <el-main class="content-layout">
      <Title />
      <Package />
    </el-main>
  </el-container>
</template>

<script>
  import Title from "./Content/Title";
  import Package from "./Content/Package";

  export default {
    name: 'Content',
    components: {
      Title,
      Package
    }
  };
</script>

<style lang="scss">
  .content-layout {
    background-color: #efefef;
    padding: 20px;
  }
</style>

