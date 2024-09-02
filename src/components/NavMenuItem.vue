<script>
export default {
    props: {
        navItem: String,
        caret: String
    }
}
</script>
<template>
    <div class="dropdown" v-if="caret">
        <li class="nav-item mx-2 d-flex" data-bs-toggle="dropdown" aria-expanded="false">
            <div class="text pe-1 mt-3">{{ navItem }}</div>
            <i :class="caret">
                <ul class="dropdown-menu">
                    <li><a class="dropdown-item" href="#">SERVICES</a></li>
                    <li><a class="dropdown-item" href="#">OUR WORK FLOW</a></li>
                    <li><a class="dropdown-item" href="#">VIDEO THUMBNAIL TYPE</a></li>
                </ul>
            </i>
        </li>
    </div>
    <div v-if="!caret">
        <li class="nav-item mx-2 d-flex">
            <div class="text pe-1 mt-3">{{ navItem }}</div>
        </li>
    </div>
</template>
<style lang="scss" scoped>
    .dropdown-item {
        color: white;
        background-color: black;
        font-size: 8px;
        padding: 10px;
    }
    .text {
        font-size: 14px;
    }
</style>