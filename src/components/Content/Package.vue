<template>
  <div class="layout-container">
    <el-row :gutter="24" justify="center" align="middle" class="no-margin">
      <el-col :xs="24" :sm="12" :md="12" :lg="12" :xl="12">
        <img src="" alt="">
      </el-col>
      <el-col :xs="12" :sm="6" :md="6" :lg="6" :xl="6" style="min-height: 100px;">
        <span v-for="(item, index) in descBasic" :key="index">
          
        </span>
      </el-col>
      <el-col :xs="12" :sm="6" :md="6" :lg="6" :xl="6" style="min-height: 100px;">
        <el-button type="primary" class="gredient-button">สมัครระบบฟรี ตลอดไป</el-button>
      </el-col>
    </el-row>
    <!-- Package list -->
    <el-row justify="space-around" align="middle">
      <el-col style="padding: 10px" :xs="24" :sm="12" :md="6" :lg="6" :xl="6" v-for="(item, idx) in isPro ? pro : basic" :key="idx">
        <div class="package-container">
          <div style="font-size: 17px; color: black;">
            {{item.title}}
          </div>
          <div style="font-size: 17px; color: black;">
            {{item.price}} ฿
          </div>
          <div>
            <span style="font-size: 12px; color: white; background-color: #555; padding: 5px; margin: 0 8px;" v-for="(pitem, ind) in item.pricePack" :key="ind">{{pitem}}</span>
          </div>
          <div style="height: 20px; padding: 28px 0 15px 0;">
            <button v-if="item.isBuyable" class="package-buyable-btn">
              Buy
            </button>
          </div>
          <div v-for="(dItem, index) in item.detail" :key="index" class="package-detail-list">
            {{dItem}}
          </div>
        </div>
      </el-col>
    </el-row>
    <el-row>
      <el-col style="text-align: center; margin: 20px 0">
        <span class="text-isPro" :style="!isPro ? 'color: #009df8;' : ''">
          รุ่นธรรมดา
        </span>
        <label class="switch">
          <input type="checkbox" v-model="isPro" checked>
          <span class="slider round"></span>
        </label>
        <span class="text-isPro" :style="isPro ? 'color: #009df8;' : ''">
          รุ่น Pro
        </span>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'Title',
  data () {
    return {
      isPro: false,
      descBasic: [
        <span class="package-title-text">สมัครวันนี้ ฟรีทันที 50 ออร์เดอร์</span>,
        <span class="package-title-text">สมัครวันนี้ ฟรีทันที 50 ออร์เดอร์</span>,
        <span class="package-title-text">สมัครวันนี้ ฟรีทันที 50 ออร์เดอร์</span>,
        <span class="package-title-text">สมัครวันนี้ ฟรีทันที 50 ออร์เดอร์</span>
        // '- ใช้งานฟรีตลอดไป',
        // '- ไม่จำกัดฟีเจอร์',
        // '- ขายของครบเครื่องทุกฟังก์ชัน'
      ],
      descPro: [
        'สมัครวันนี้ ฟรีทันที 50 ออร์เดอร์',
        '- ใช้งานฟรีตลอดไป',
        '- ไม่จำกัดฟีเจอร์',
        '- ขายของครบเครื่องทุกฟังก์ชัน'
      ],
      basic: [
        {
          title: 'เริ่มต้น',
          price: 0,
          isBuyable: false,
          pricePack: [
            'ฟรีตลอดไป'
          ],
          detail: [
            '50 ออเดอร์/เดือน',
            '1 Admin',
            '1 คลังสินค้า',
            '0 ตัวแทนจำหน่าย',
            'ไม่จำกัด รายการสินค้า'
          ]
        },
        {
          title: 'ร้านขนาดกลาง',
          price: 450,
          isBuyable: true,
          pricePack: [
            '1200 บาท / 3 เดือน',
            '4700 บาท / 1 ปี',
          ],
          detail: [
            '150 ออเดอร์/เดือน',
            '3 Admin',
            '1 คลังสินค้า',
            '4 ตัวแทนจำหน่าย',
            'ไม่จำกัด รายการสินค้า'
          ]
        },
        {
          title: 'ร้านขนาดใหญ่',
          price: 650,
          isBuyable: true,
          pricePack: [
            '1800 บาท / 3 เดือน',
            '6900 บาท / 1 ปี',
          ],
          detail: [
            '300 ออเดอร์/เดือน',
            '6 Admin',
            '1 คลังสินค้า',
            '8 ตัวแทนจำหน่าย',
            'ไม่จำกัด รายการสินค้า'
          ]
        },
        {
          title: 'ไม่จำกัด',
          price: 850,
          isBuyable: true,
          isBuyable: true,
          pricePack: [
            '6900 บาท / 3 เดือน',
            '8900 บาท / 1 ปี',
          ],
          detail: [
            'ไม่จำกัด ออเดอร์/เดือน',
            '10 Admin',
            '1 คลังสินค้า',
            '10 ตัวแทนจำหน่าย',
            'ไม่จำกัด รายการสินค้า'
          ]
        },
      ],
      pro: [
        {
          title: 'Quiet Pro',
          price: 890,
          isBuyable: true,
          pricePack: [
            '2600 บาท / 3 เดือน',
            '8900 บาท / 1 ปี',
          ],
          detail: [
            'ไม่จำกัด ออเดอร์/เดือน',
            '10 Admin',
            '1 คลังสินค้า',
            '0 ตัวแทนจำหน่าย',
            'ไม่จำกัด รายการสินค้า'
          ]
        },
        {
          title: 'Pro',
          price: 1190,
          isBuyable: true,
          pricePack: [
            '3400 บาท / 3 เดือน',
            '11900 บาท / 1 ปี',
          ],
          detail: [
            'ไม่จำกัด ออเดอร์/เดือน',
            '15 Admin',
            '2 คลังสินค้า',
            '15 ตัวแทนจำหน่าย',
            'ไม่จำกัด รายการสินค้า'
          ]
        },
        {
          title: 'Truely Pro',
          price: 1590,
          isBuyable: true,
          pricePack: [
            '4600 บาท / 3 เดือน',
            '15900 บาท / 1 ปี',
          ],
          detail: [
            'ไม่จำกัด ออเดอร์/เดือน',
            '20 Admin',
            '3 คลังสินค้า',
            '30 ตัวแทนจำหน่าย',
            'ไม่จำกัด รายการสินค้า'
          ]
        },
        {
          title: 'Extreamly Pro',
          price: 1990,
          isBuyable: true,
          pricePack: [
            '5800 บาท / 3 เดือน',
            '19900 บาท / 1 ปี',
          ],
          detail: [
            'ไม่จำกัด ออเดอร์/เดือน',
            'ไม่จำกัด Admin',
            'ไม่จำกัด คลังสินค้า',
            'ไม่จำกัด ตัวแทนจำหน่าย',
            'ไม่จำกัด รายการสินค้า'
          ]
        },
      ]
    }
  }
};
</script>

<style lang="scss">
  .no-margin {
    margin: 0!important;
  }

  .switch {
    position: relative;
    display: inline-block;
    width: 100px;
    height: 28px;
  }

  .switch input { 
    opacity: 0;
    width: 0;
    height: 0;
  }

  .slider {
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-image: linear-gradient(#00d6cb, #009df8);
    -webkit-transition: .4s;
    transition: .4s;
  }

  .slider:before {
    position: absolute;
    content: "";
    height: 21px;
    width: 21px;
    left: 4px;
    bottom: 4px;
    background-color: white;
    -webkit-transition: .4s;
    transition: .4s;
  }

  input:checked + .slider {
    background-image: linear-gradient(#00d6cb, #009df8);
  }

  input:focus + .slider {
    box-shadow: 0 0 1px #2196F3;
  }

  input:checked + .slider:before {
    -webkit-transform: translateX(71px);
    -ms-transform: translateX(71px);
    transform: translateX(71px);
  }

  /* Rounded sliders */
  .slider.round {
    border-radius: 34px;
  }

  .slider.round:before {
    border-radius: 50%;
  }

  .layout-container {
    background-color: white;
    width: 100%;
    margin: 20px 0 0 0;
    padding: 24px 0 24px 0;
  }

  .package-title-text {
    min-height: 100px;
    color: rgb(0, 146, 127);
  }

  .gredient-button {
    background-image: linear-gradient(#00d6cb, #009df8);
    border: none;
  }
  
  .gredient-button:hover {
    background-image: linear-gradient(#00e2d7, #3eb8ff);
    background-position: left right;
  }

  .gredient-button:active {
    background-image: linear-gradient(#00a59d, #007dc5);
    background-position: left right;
  }
  
  .gredient-button:focus {
    background-image: linear-gradient(#00a59d, #007dc5);
    background-position: left right;
  }
  
  .package-card {
    border: 0.1px #aaa solid;
  }

  .package-container {
    padding: 15px 10px;
    border: 1px solid #ccc;
    text-align: center;
  }

  .package-detail-list {
    margin: 15px 20px 15px 20px;
    border-bottom: 1px solid #ccc;
    color: rgb(0, 146, 127);
  }

  .package-buyable-btn {
    background: none;
    background-color: Transparent;
    background-repeat:no-repeat;
    outline: none;
    font-size: 15px;
    font-weight: bold; 
    color: rgb(0, 146, 127);
    border: rgb(0, 146, 127) 1px solid;
    border-radius: 17px;
    padding: 7px 45px;
    // box-shadow: 0px 3px 3px #888888;
    cursor: pointer;

    &:hover {
      color: rgb(0, 182, 158);
    border: rgb(0, 182, 158) 1px solid;
    }
  }

  .text-isPro {
    margin: 0 20px;
  }
</style>
