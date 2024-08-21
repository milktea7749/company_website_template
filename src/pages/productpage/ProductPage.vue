<template>
  <div>
    <common-banner :imgSrc="imgPath" :imgLabel="imgLabel"></common-banner>
    <common-main @clickSideMenu="handleSideClick" :title="imgLabel" :menus="sideMenus">
      <div slot="content">
        <list-page :dataSource="dataSource"></list-page>
      </div>
    </common-main>
  </div>
</template>

<script>
import CommonBanner from '@/pages/common/Banner'
import CommonMain from '@/pages/common/Main'
import ListPage from './components/List'
export default {
  name: 'ProductPage',
  components: {
    CommonBanner,
    CommonMain,
    ListPage
  },
  data() {
    return {
      imgPath: '/static/img/banner3.jpg',
      imgLabel: '主要商品 / 服務項目',
      dataSource: [],
      sideMenus: [
        {
          id: 'side1',
          key: 'ProductList',
          label: '技術諮詢'
        },
        {
          id: 'side2',
          key: 'ServiceList',
          label: '人才訓練'
        },
        {
          id: 'side3',
          key: 'overseasCoOperationList',
          label: '跨國合作'
        }
      ],
      activeComponentName: 'ProductList',
      slide1:[
        {
          id: 'product1',
          imgSrc: '/static/img/home1.jpg',
          label: 'Big Data解決方案'
        },
        {
          id: 'product2',
          imgSrc: '/static/img/home1.jpg',
          label: 'IT服務與資料庫管理'
        },
        {
          id: 'product3',
          imgSrc: '/static/img/home1.jpg',
          label: '資訊安全應用'
        },
        {
          id: 'product4',
          imgSrc: '/static/img/home1.jpg',
          label: '委外服務應用'
        },
      ],
      slide2:[
        {
          id: 'service1',
          imgSrc: '/static/img/home1.jpg',
          label: '專業IT教育訓練'
        },
        {
          id: 'service2',
          imgSrc: '/static/img/home1.jpg',
          label: '企業內部培訓'
        },
        {
          id: 'service3',
          imgSrc: '/static/img/home1.jpg',
          label: '產學合作實習訓練'
        }
      ], 
      slide3:[
        {
          id: 'service1',
          imgSrc: '/static/img/home1.jpg',
          label: '打造科技人才從訓練到實體就業一條龍完整平台'
        },
        {
          id: 'service2',
          imgSrc: '/static/img/home1.jpg',
          label: '整合國際企業間合作'
        }
      ]
    }
  },
  methods: {
    handleSideClick(name) {
      this.activeComponentName = name
      if (name === 'ProductList') {
        this.dataSource = this.slide1
      } else if (name === 'ServiceList') {
        this.dataSource = this.slide2
      } else if (name === 'overseasCoOperationList') {
        this.dataSource = this.slide3
      } else {
        this.dataSource = this.slide1
      }
    }
  },
  mounted(){
    this.handleSideClick()
  }
}
</script>
