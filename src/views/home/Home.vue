<template>
<div>
    <h2>Home</h2>
    <p>Welcome, {{ username }}!</p>
    <button @click="logout">Logout</button>
</div>
</template>

<script setup lang="ts">
import { computed } from 'vue';

// 使用 computed 来获取 Pinia 中的状态
const username = computed(() => {
    return $store.auth.username;
});

const logout = () => {
    // 清除登录状态，可以是清除 Pinia 中的用户信息等
    $store.auth.logout()
    .then(() => {
    // 登出成功后跳转到登录页
    $router.push({ name: 'Login' });
    })
    .catch(error => {
    console.error('Logout failed:', error);
    });
};

</script>
