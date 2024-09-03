<script>
export default {
    props: {
        icon: String,
        info: String
    }
}
</script>
<template>
    <div>
        <li class="info-item">
            <i :class="icon"></i>
            <span class="text">{{ info }}</span>
        </li>
    </div>
</template>
<style lang="scss" scoped>
    .info-item:hover {
        color: white;
    }
</style>