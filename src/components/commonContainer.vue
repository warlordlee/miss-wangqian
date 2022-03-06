<template>
    <div class="common-container">
        <slot></slot>
    </div>
</template>

<script>
    export default {
        name: "common-container"
    }
</script>

<style scoped lang="less">
    .common-container {
        position: relative;
        background-color: #B33929;
        width: 100%;
        height: 100%;
        overflow: hidden;
    }

    common-container img {
        width: 100%;
        height: 100%;
    }
</style>
