<script setup lang="ts">

const linkUrl = (subdomain: string) => {
  window.location.href = 'https://' + subdomain + '.itwray.com';
}
</script>

<template>
  <div class="main-layout">
    <el-container>
      <el-main class="main-container">
        <div>
          <el-button type="primary" @click="linkUrl('blog')">个人博客</el-button>
          <el-button type="success" @click="linkUrl('eat')">点餐系统</el-button>
        </div>
      </el-main>
      <el-footer class="footer">
        <div class="footer-content">
          <a href="https://beian.miit.gov.cn/"><span>鄂ICP备2024050235号-1</span></a>&nbsp;&nbsp;
          <a href="https://beian.mps.gov.cn/#/query/webSearch?code=42018502007471" rel="noreferrer" target="_blank">
            <el-image src="https://itwray-bucket.oss-cn-wuhan-lr.aliyuncs.com/img/beian.png"
                      style="width: 15px; height: 15px" fit='contain'/>
            <span>鄂公网安备42018502007471</span>
          </a>
        </div>
      </el-footer>
    </el-container>
  </div>
</template>

<style scoped>
.main-layout {
  height: 100vh; /* 设置高度为视口高度，使布局充满整个浏览器窗口 */
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.main-container {
  height: 100%; /* 设置高度为视口高度，使布局充满整个浏览器窗口 */
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>