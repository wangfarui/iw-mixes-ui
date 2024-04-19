<script setup lang="ts">

const linkUrl = (subdomain: string) => {
  window.location.href = 'https://' + subdomain +'.itwray.com';
}
</script>

<template>
  <main>
    <div class="container">
      <div class="mb-4">
        <el-button type="primary" @click="linkUrl('blog')">个人博客</el-button>
        <el-button type="success" @click="linkUrl('eat')">点餐系统</el-button>
      </div>
    </div>
  </main>
</template>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
</style>