<script>
export default {
    props: {
        navItem: String,
        caret: String
    }
}
</script>
<template>
    <div class="dropdown">
        <li class="nav-item mx-1 d-flex dropdown-toggle" data-bs-toggle="dropdown" aria-expanded="false">
            <div class="text">{{ navItem }}</div>
            <i :class="caret"></i>
            <ul class="dropdown-menu">
                <li><a class="dropdown-item" href="#">SERVICES</a></li>
                <li><a class="dropdown-item" href="#">OUR WORK FLOW</a></li>
                <li><a class="dropdown-item" href="#">VIDEO THUMBNAIL TYPE</a></li>
            </ul>
        </li>
    </div>
</template>
<style lang="scss" scoped>
    .dropdown-item {
        color: white;
        background-color: black;
        font-size: 12px;
        padding: 10px;
    }
</style>