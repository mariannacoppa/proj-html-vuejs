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
                    <div class="icons">
                        <i class="fa-solid fa-magnifying-glass"></i>
                        <!-- <span><hr class="text-white"></span> -->
                        <i class="ms-1 fa-brands fa-facebook-f"></i>
                        <i class="ms-1 fa-brands fa-twitter"></i>
                        <i class="ms-1 fa-brands fa-youtube"></i>
                        <i class="ms-1 fa-brands fa-instagram"></i>

                    </div>
                </div>
            </div>
        </div>
    </header>
</template>
<style lang="scss" scoped>
    i, .caret {
        width: 30px;
    };
    .fa-magnifying-glass {
        border-right: 2px solid lightgray;
        margin-right: 10px;
    }
</style>