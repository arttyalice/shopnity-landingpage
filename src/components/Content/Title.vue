<template>
  <span>
    <el-row>
      <el-col>
        <span class="title-text">ราคาแพ็คเก็จ</span> <span class="title-sub-text">(เลือกให้ดีที่สุดฉบับธุรกิจคุณ)</span> 
      </el-col>
    </el-row>
    <el-row>
      <el-col>
        <span class="title-desc-text">
          * ตัวแทนจำหน่ายของร้าน สามารถมี user ของตัวเองเพื่อเข้ามาสร้างออเดอร์, เช็คสต็อค, ดูประวัติ, ยอดขายของตัวเองได้
        </span>
      </el-col>
    </el-row>
  </span>
</template>

<script>
export default {
  name: 'Title',
};
</script>

<style lang="scss">
  .title-text {
    color: rgb(59, 59, 68);
    font-size: 24px;
    margin: 0 0 0 20px;
  }
  .title-sub-text {
    color: rgb(199, 32, 32);
    font-size: 14px;
    margin: 0 0 0 10px;
  }
  .title-desc-text {
    color: rgb(117, 18, 18);
    font-size: 13px;
    margin: 0 0 0 20px;
  }
  @media screen and (max-width: 689px) {
    .title-text {
      margin: 0 0 0 0px;
    }
    .title-sub-text {
      margin: 0 0 0 10px;
    }
    .title-desc-text {
      margin: 0 0 0 0px;
    }
  }
</style>

