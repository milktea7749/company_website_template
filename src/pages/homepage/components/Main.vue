<template>
  <el-container :class="containerClass">
    <el-main>
      <h2>万十科技股份有限公司</h2>

      <h2>經營理念</h2>
      <p>「Recode your thinking & Decode in ONCE」</p>
      <p>公司以整合國際科技人才為目標，同時並積極推動人才跨域轉型，公司與台日多間企業及學校合作，在人才訓練上給予協助合作。</p>
      <p>透過以「人」為主體，建立產業、官方、學術界緊密的關係。優秀人才的產出銜接合作企業的業務需求、推動企業間的擴大發展進而再尋求優秀人才的協助，成為一個無止盡的正向循環發展，打造不是以技術而以「人」為中心的科技產業。</p>

      <h2>主要商品 / 服務項目</h2>
      <h3>技術諮詢</h3>
      <ul>
        <li>Big Data解決方案</li>
        <li>IT服務與資料庫管理</li>
        <li>資訊安全應用</li>
        <li>委外服務應用</li>
      </ul>

      <h3>人才訓練</h3>
      <ul>
        <li>專業IT教育訓練</li>
        <li>企業內部培訓</li>
        <li>產學合作實習訓練</li>
      </ul>

      <h3>跨國合作</h3>
      <ul>
        <li>打造科技人才從訓練到實體就業一條龍完整平台</li>
        <li>整合國際企業間合作</li>
      </ul>

      <div class="img-box">
        <img src="/static/img/home1.jpg" alt="company-concept">
      </div>
    </el-main>
  </el-container>
</template>

<script>
export default {
  name: 'HomeMain',
  computed: {
    containerClass() {
      return this.$ISMOBILE ? '' : 'container'
    }
  }
}
</script>

<style scoped>
.container {
  padding: 0 6rem;
}

.el-container p {
  line-height: 1.5;
  text-align: justify;
}

.img-box {
  padding: 2rem 0;
}

.img-box img {
  height: 30rem;
  width: 100%;
}
</style>
