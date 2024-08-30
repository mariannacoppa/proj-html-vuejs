<script>
import NavMenuItems from '../../navMenuItems.json';
import NavMenuItem from './NavMenuItem.vue';
export default {
    components: {
        NavMenuItem
    },
    data () {
        return {
            navobjs: NavMenuItems
        }
    }
}
</script>
<template>
    <header class="container">
        <div class="row">
            <div class="col-12">
                <div class="navbar d-flex justify-content-between">
                    <div class="logo">logo</div>
                    <div class="nav-menu">
                        <div class="nav-items">
                            <ul class="d-flex list-unstyled">
                                <NavMenuItem class="navItem" v-for="(navobj, index) in navobjs" :navItem="navobj.navItem" :caret="navobj.caret"/>
                                <!-- <li class="mx-1">icona 1</li>
                                <li class="mx-1">icona 2</li> -->
                            </ul>
                            <!-- <div class="caret">&#xF282;</div>
                            <i class="bi bi-chevron-down"></i> -->
                        </div>
                    </div>
                    <div class="icons">social
                        <i class="fas fa-phone"></i>
                        <i class="fas fa-facebook"></i>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>
<style lang="scss" scoped>
    i, .caret {
        background-color: black;
        color: white;
        padding: 10px;
        width: 30px;
    }
</style>