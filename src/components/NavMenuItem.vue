<script>
export default {
    props: {
        navItem: String,
        caret: String
    }
}
</script>
<template>
    <div>
        <li class="nav-item mx-1 d-flex">
            <div class="text">{{ navItem }}</div>
            <div class="chevron">{{ caret }}</div>
        </li>
    </div>
</template>
<style lang="scss" scoped>
    .nav-item:hover:nth-child(3) {
        color: red;
    }
</style>