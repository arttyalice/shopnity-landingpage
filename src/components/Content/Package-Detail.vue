<template>
  <div class="layout-container">
    <el-row :gutter="24" style="padding: 10px;" justify="center" align="middle" class="no-margin">
      <el-col :xs="9" :sm="9" :md="9" :lg="9" :xl="9">
        <img src="" alt="">
      </el-col>
      <el-col :span="5" class="center-text" style="font-size: 18px; color: #00d6cb;">
        เริ่มต้น
      </el-col>
      <el-col :span="5" class="center-text" style="font-size: 18px; color: #009df8;">
        รุ่นธรรมดา
      </el-col>
      <el-col :span="5" class="center-text" style="font-size: 18px; color: rgb(31, 46, 255);">
        รุ่น Pro
      </el-col>
    </el-row>
    <el-row :gutter="24" style="padding: 10px;" justify="center" align="middle" class="no-margin">
      <el-col :span="9" style="color: Black; font-size: 36px; font-weight: 300;">
        Key<br>Feature
      </el-col>
      <el-col :span="5" class="center-text">
        <img src="" alt="">
      </el-col>
      <el-col :span="5" class="center-text">
        <img src="" alt="">
      </el-col>
      <el-col :span="5" class="center-text">
        <img src="" alt="">
      </el-col>
    </el-row>
    <!-- ระบบออเดอร์ -->
    <el-row :gutter="24" style="padding: 20px 20px 5px 20px;">
      <el-col :span="9" class="detail-header-text">ระบบออเดอร์</el-col>
    </el-row>
    <el-row :gutter="24" style="padding: 0px 20px;" justify="center" align="middle" class="no-margin" v-for="(item, index) in detailOrder" :key="index">
      <el-col :span="9" class="a-detail-title">
        {{item.title}}
      </el-col>
      <el-col :span="5" class="center-text">
        <i :class="item.got1 ? 'el-icon-check a-detail-symbol' : 'el-icon-close a-detail-symbol-not'"></i>
      </el-col>
      <el-col :span="5" class="center-text">
        <i :class="item.got2 ? 'el-icon-check a-detail-symbol' : 'el-icon-close a-detail-symbol-not'"></i>
      </el-col>
      <el-col :span="5" class="center-text">
        <i :class="item.got3 ? 'el-icon-check a-detail-symbol' : 'el-icon-close a-detail-symbol-not'"></i>
      </el-col>
    </el-row>
    <!-- ระบบสต็อกสินค้า-->
    <el-row :gutter="24" style="padding: 20px 20px 5px 20px;">
      <el-col :span="9" class="detail-header-text">ระบบสต็อกสินค้า</el-col>
    </el-row>
    <el-row :gutter="24" style="padding: 0px 20px;" justify="center" align="middle" class="no-margin" v-for="(item, index) in detailStock" :key="index">
      <el-col :span="9" class="a-detail-title">
        {{item.title}}
      </el-col>
      <el-col :span="5" class="center-text">
        <i :class="item.got1 ? 'el-icon-check a-detail-symbol' : 'el-icon-close a-detail-symbol-not'"></i>
      </el-col>
      <el-col :span="5" class="center-text">
        <i :class="item.got2 ? 'el-icon-check a-detail-symbol' : 'el-icon-close a-detail-symbol-not'"></i>
      </el-col>
      <el-col :span="5" class="center-text">
        <i :class="item.got3 ? 'el-icon-check a-detail-symbol' : 'el-icon-close a-detail-symbol-not'"></i>
      </el-col>
    </el-row>
    <!-- ระบบแพ็คสินค้า - จัดส่ง -->
    <el-row :gutter="24" style="padding: 20px 20px 5px 20px;">
      <el-col :span="9" class="detail-header-text">ระบบแพ็คสินค้า - จัดส่ง</el-col>
    </el-row>
    <el-row :gutter="24" style="padding: 0px 20px;" justify="center" align="middle" class="no-margin" v-for="(item, index) in detailPack" :key="index">
      <el-col :span="9" class="a-detail-title">
        {{item.title}}
      </el-col>
      <el-col :span="5" class="center-text">
        <i :class="item.got1 ? 'el-icon-check a-detail-symbol' : 'el-icon-close a-detail-symbol-not'"></i>
      </el-col>
      <el-col :span="5" class="center-text">
        <i :class="item.got2 ? 'el-icon-check a-detail-symbol' : 'el-icon-close a-detail-symbol-not'"></i>
      </el-col>
      <el-col :span="5" class="center-text">
        <i :class="item.got3 ? 'el-icon-check a-detail-symbol' : 'el-icon-close a-detail-symbol-not'"></i>
      </el-col>
    </el-row>
    <!-- ระบบรายงานสถิติและการเงิน -->
    <el-row :gutter="24" style="padding: 20px 20px 5px 20px;">
      <el-col :span="9" class="detail-header-text">ระบบรายงานสถิติและการเงิน</el-col>
    </el-row>
    <el-row :gutter="24" style="padding: 0px 20px;" justify="center" align="middle" class="no-margin" v-for="(item, index) in detailStatistic" :key="index">
      <el-col :span="9" class="a-detail-title">
        {{item.title}}
      </el-col>
      <el-col :span="5" class="center-text">
        <i :class="item.got1 ? 'el-icon-check a-detail-symbol' : 'el-icon-close a-detail-symbol-not'"></i>
      </el-col>
      <el-col :span="5" class="center-text">
        <i :class="item.got2 ? 'el-icon-check a-detail-symbol' : 'el-icon-close a-detail-symbol-not'"></i>
      </el-col>
      <el-col :span="5" class="center-text">
        <i :class="item.got3 ? 'el-icon-check a-detail-symbol' : 'el-icon-close a-detail-symbol-not'"></i>
      </el-col>
    </el-row>
    <!-- ระบบตัวแทนจำหน่าย -->
    <el-row :gutter="24" style="padding: 20px 20px 5px 20px;">
      <el-col :span="9" class="detail-header-text">ระบบตัวแทนจำหน่าย</el-col>
    </el-row>
    <el-row :gutter="24" style="padding: 0px 20px;" justify="center" align="middle" class="no-margin" v-for="(item, index) in detailAgent" :key="index">
      <el-col :span="9" class="a-detail-title">
        {{item.title}}
      </el-col>
      <el-col :span="5" class="center-text">
        <i :class="item.got1 ? 'el-icon-check a-detail-symbol' : 'el-icon-close a-detail-symbol-not'"></i>
      </el-col>
      <el-col :span="5" class="center-text">
        <i :class="item.got2 ? 'el-icon-check a-detail-symbol' : 'el-icon-close a-detail-symbol-not'"></i>
      </el-col>
      <el-col :span="5" class="center-text">
        <i :class="item.got3 ? 'el-icon-check a-detail-symbol' : 'el-icon-close a-detail-symbol-not'"></i>
      </el-col>
    </el-row>
    <!-- สะดวกลูกค้า -->
    <el-row :gutter="24" style="padding: 20px 20px 5px 20px;">
      <el-col :span="9" class="detail-header-text">สะดวกลูกค้า</el-col>
    </el-row>
    <el-row :gutter="24" style="padding: 0px 20px;" justify="center" align="middle" class="no-margin" v-for="(item, index) in detailBuyer" :key="index">
      <el-col :span="9" class="a-detail-title">
        {{item.title}}
      </el-col>
      <el-col :span="5" class="center-text">
        <i :class="item.got1 ? 'el-icon-check a-detail-symbol' : 'el-icon-close a-detail-symbol-not'"></i>
      </el-col>
      <el-col :span="5" class="center-text">
        <i :class="item.got2 ? 'el-icon-check a-detail-symbol' : 'el-icon-close a-detail-symbol-not'"></i>
      </el-col>
      <el-col :span="5" class="center-text">
        <i :class="item.got3 ? 'el-icon-check a-detail-symbol' : 'el-icon-close a-detail-symbol-not'"></i>
      </el-col>
    </el-row>
    <!-- สะดวกแม่ค้า -->
    <el-row :gutter="24" style="padding: 20px 20px 5px 20px;">
      <el-col :span="9" class="detail-header-text">สะดวกแม่ค้า</el-col>
    </el-row>
    <el-row :gutter="24" style="padding: 0px 20px;" justify="center" align="middle" class="no-margin" v-for="(item, index) in detailSelf" :key="index">
      <el-col :span="9" class="a-detail-title">
        {{item.title}}
      </el-col>
      <el-col :span="5" class="center-text">
        <i :class="item.got1 ? 'el-icon-check a-detail-symbol' : 'el-icon-close a-detail-symbol-not'"></i>
      </el-col>
      <el-col :span="5" class="center-text">
        <i :class="item.got2 ? 'el-icon-check a-detail-symbol' : 'el-icon-close a-detail-symbol-not'"></i>
      </el-col>
      <el-col :span="5" class="center-text">
        <i :class="item.got3 ? 'el-icon-check a-detail-symbol' : 'el-icon-close a-detail-symbol-not'"></i>
      </el-col>
    </el-row>
    <el-row :gutter="24" style="padding: 0px 20px;" justify="center" align="middle" class="no-margin">
      <el-col :span="9" class="a-detail-title">
        เติมเครดิตในระบบ (แจ้งพัสดุอัตโนมัติ)
      </el-col>
      <el-col :span="15" class="center-text" style="padding-top: 15px;">
        <span>1.5 บาท/70ตัวอักษร</span><span class="a-red-chip">ถูกที่สุด</span>
      </el-col>
    </el-row>
    <!-- Support พลังแม่ค้า -->
    <el-row :gutter="24" style="padding: 20px 20px 5px 20px;">
      <el-col :span="9" class="detail-header-text">Support พลังแม่ค้า</el-col>
    </el-row>
    <el-row :gutter="24" style="padding: 0px 20px;" justify="center" align="middle" class="no-margin">
      <el-col :span="9" class="a-detail-title">
        การช่วยเหลือทางเทคนิค
      </el-col>
      <el-col :span="15" class="center-text" style="padding-top: 7px;">
        <span style="border-bottom: 1px #ccc solid; padding-bottom: 7px;">ทุกแพ็คเกจ จะได้ความช่วยเหลือทุกช่องทาง ทั้ง Line@ FB และเบอร์โทร</span>
      </el-col>
    </el-row>
    <el-row :gutter="24" style="padding: 0px 20px;" justify="center" align="middle" class="no-margin">
      <el-col :span="9" class="a-detail-title" style="border: none;">
        ความปลอดภัยมาตรฐานสากลโลก
      </el-col>
      <el-col :span="15" class="center-text" style="padding-top: 7px;">
        <span>ข้อมูลปลอดภัยด้วยมาตรฐานเทคโนโลยีระดับโลก</span>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'Package-Detail',
  data () {
    return {
      detailOrder: [
        {title: 'Admin (User) ทำงานหลายคน', got1: true, got2: true, got3: true},
        {title: 'สถานะชำระเงิน,ส่งสินค้าของลูกค้า', got1: true, got2: true, got3: true},
        {title: 'บันทึกชื่อ ที่อยู่ เบอร์โทรลูกค้า เลขผู้เสียภาษี', got1: true, got2: true, got3: true},
        {title: 'แสดงประวัติลูกค้าที่เคยซื้อทั้งหมด', got1: true, got2: true, got3: true},
        {title: 'ใบเสร็จ/ใบกำกับภาษี', got1: true, got2: true, got3: true},
        {title: 'Import/Export ข้อมูลลูกค้า', got1: false, got2: true, got3: true},
        {title: 'คำนวนส่วนลดให้แต่ละกลุ่มลูกค้าอัตโนมัติ', got1: true, got2: true, got3: true},
        {title: 'สรุปคำสั่งซื้อ', got1: true, got2: true, got3: true},
        {title: 'ระบบ Pos ขายหน้าร้าน', got1: false, got2: false, got3: true},
      ],
      detailStock: [
        {title: 'จำนวนรายการสินค้า', got1: 'infi', got2: 'infi', got3: 'infi'},
        {title: 'Barcode สินค้า', got1: true, got2: true, got3: true},
        {title: 'เพิ่มสต็อกด้วย Excel', got1: false, got2: true, got3: true},
        {title: 'สินค้าหลักและสินค้าย่อย', got1: true, got2: true, got3: true},
        {title: 'แสดงต้นทุนสินค้ารวมและต่อชิ้น', got1: true, got2: true, got3: true},
        {title: 'กำหนดอายุใบสั่งซื้อ', got1: false, got2: true, got3: true},
        {title: 'แจ้งเตือนสินค้าใกล้หมด', got1: true, got2: true, got3: true},
        {title: 'แสดงประวัติการเพิ่มสินค้า', got1: true, got2: true, got3: true},
        {title: 'สร้าง Barcode สินค้า', got1: false, got2: false, got3: true},
        {title: 'บันทึกข้อมูล Supplier', got1: false, got2: false, got3: true},
        {title: 'Import/Export รายการสินค้า,หมวดหมู่สินค้า', got1: false, got2: false, got3: true},
      ],
      detailPack: [
        {title: 'จำนวนรายการสินค้า', got1: true, got2: true, got3: true},
        {title: 'Barcode สินค้า', got1: true, got2: true, got3: true},
        {title: 'แสดงประวัติการเพิ่มสต็อกสินค้า', got1: true, got2: true, got3: true},
        {title: 'แจ้งเตือนสินค้าใกล้หมด', got1: true, got2: true, got3: true},
        {title: 'สินค้าหลักและสินค้าย่อย', got1: true, got2: true, got3: true},
        {title: 'แสดงต้นทุนสินค้ารวมและต่อชิ้น', got1: true, got2: true, got3: true},
        {title: 'กำหนดใบสั่งซื้อ', got1: true, got2: true, got3: true},
      ],
      detailStatistic: [
        {title: 'การเงินพื้นฐาน', got1: true, got2: true, got3: true},
        {title: 'รายงานสถิติ', got1: true, got2: true, got3: true},
        {title: 'Export รายงานเป็น Excel', got1: false, got2: true, got3: true},
        {title: 'รายงาน Cash Flow', got1: false, got2: false, got3: true},
        {title: 'ประวัติรายงาน', got1: true, got2: true, got3: true},
      ],
      detailAgent: [
        {title: 'ตัวแทนฯ สั่งของด้วยตัวเอง', got1: false, got2: true, got3: true},
        {title: 'ตั้งค่ากำหนดขั้นแต่ละตัวแทนได้', got1: false, got2: true, got3: true},
        {title: 'ตัวแทน Drop Ship', got1: false, got2: true, got3: true},
      ],
      detailBuyer: [
        {title: 'การชำระเงินผ่านบัตรเครดิต', got1: true, got2: true, got3: true},
        {title: 'ชำระเงินผ่านธนาคาร', got1: true, got2: true, got3: true},
        {title: 'บริการเก็บเงินปลายทาง COD', got1: true, got2: true, got3: true},
      ],
      detailSelf: [
        {title: 'เชื่อมต่อกับ SCG Express', got1: true, got2: true, got3: true},
        {title: 'เชื่อมต่อ APIs ระบบภายนอก (Wordpress,Woocommerce ฯลฯ)', got1: false, got2: true, got3: true},
        {title: 'บริการ Drop-off กับไปรษณีย์ไทย', got1: true, got2: true, got3: true},
      ],
    }
  }
};
</script>

<style lang="scss">
  .layout-container {
    background-color: white;
    width: 100%;
    margin: 20px 0 0 0;
    padding: 24px 10px 24px 10px;
  }

  .no-margin {
    margin: 0!important;
  }

  .center-text {
    text-align: center;
  }

  .detail-header-text {
    font-size: 18px;
    color: black;
  }

  .a-detail-title {
    padding: 7px 0;
    border-bottom: 1px #ccc solid;
    font-size: 16px;
    font-weight: 200;
    color: black;
  }

  .a-detail-symbol {
    border-bottom: 1px #ccc solid;
    width: 60px;
    font-size: 24px;
    font-weight: bold;
    color: #00d6cb;
    padding: 7px 0;
  }

  .a-detail-symbol-not {
    border-bottom: 1px #ccc solid;
    width: 60px;
    font-size: 24px;
    font-weight: bold;
    color: #d84a68;
    padding: 7px 0;
  }

  .a-red-chip {
    background-color: red;
    color: white;
    border-radius: 15px;
    font-size: 12px;
    padding: 2px 15px 2px 15px;
    margin-left: 24px;
  }
</style>
