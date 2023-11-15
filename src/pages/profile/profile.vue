<script lang="ts" setup>
    import { useInit } from '@/hooks/useInit'
    import { UniCard } from '@uni-helper/uni-ui-types'
    const aa = reactive({
        A: 1,
    })
    onLoad(() => {
        const { pageName, pagePath, pageQuery } = useInit()
        console.log(pageName, pagePath, pageQuery, 'pageName,pagePath, pageQuery')
    })
    const a = ref<UniCard>()
</script>

<template>
    <div>
        <wd-button>主要按钮</wd-button>
        <wd-button type="success">成功按钮</wd-button>
        <wd-button type="info">信息按钮</wd-button>
        <wd-button plain :block="true">警告按钮</wd-button>
        <wd-button type="error">危险按钮</wd-button>
    </div>
</template>

<style lang="scss" scoped></style>
