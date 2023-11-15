<template>
    <div>
        <uni-card title="ss"> </uni-card>
        <UniCard />
    </div>
</template>

<script setup>
    // 配置了自动导入
    const testStore = useStore('user')
    const a = testStore.userInfo
    const setupStore = useStore('setup')
    const { name } = setupStore
    console.log('testStore', a.value)
    onShow(() => {
        console.log('setupStore==name', name.value)
    })
</script>

<style lang="scss" scoped></style>
