<template>
  <el-container>
    <el-main>
      <h3>公司名稱</h3>
      <p>地址：台南市仁德區蔦松二街</p>
      <p>電話：</p>
      <div class="img-box">
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d58742.829610174405!2d120.18270153619798!3d23.04480745894495!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x346e70ade4e4001d%3A0x2d78267a6a53ae46!2zNzEw5Y-w54Gj5Y-w5Y2X5biC5rC45bq35Y2A6JSm5p2-!5e0!3m2!1szh-TW!2sjp!4v1724257438879!5m2!1szh-TW!2sjp" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
      </div>
    </el-main>
  </el-container>
</template>

<script>
export default {
  name: 'ContactUs'
}
</script>

<style scoped>
.el-main {
  padding: 0;
}
.img-box img {
  width: 100%;
}
.el-main p {
  line-height: 1.5;
  font-size: 1rem;
}
</style>
