<script>
export default {
    props: {
        link: String
    }
}
</script>
<template>
    <div>
        <li class="footer-link py-1">{{ link }}</li>
    </div>
</template>
<style lang="scss">
    .footer-link:hover {
        color: white;
    }
</style>