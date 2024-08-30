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
            <span class="icon">{{ icon }}</span>
            <span class="text">{{ info }}</span>
        </li>
    </div>
</template>
<style lang="">
    
</style>