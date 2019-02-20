<template>
  <div>
    <div class="content-layout">
      <Title />
      <Package />
      <PackageDetail />
    </div>
  </div>
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
    padding: 0 20px 20px 20px;
  }
</style>

