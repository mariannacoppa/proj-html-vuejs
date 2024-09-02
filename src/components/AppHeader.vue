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
                    <div class="logo">
                        <img src="../../assets/logo.svg" alt="">
                    </div>
                    <div class="nav-menu">
                        <div class="nav-items">
                            <ul class="d-flex list-unstyled">
                                <NavMenuItem class="navItem pt-3" v-for="(navobj, index) in navobjs" :caret="navobj.class" :navItem="navobj.navItem"/>
                            </ul>
                        </div>
                    </div>
                    <div class="icons">
                        <i class="fa-solid fa-magnifying-glass"/>
                        <i class="ms-1 fa-brands fa-facebook-f"/>
                        <i class="ms-1 fa-brands fa-twitter"/>
                        <i class="ms-1 fa-brands fa-youtube"/>
                        <i class="ms-1 fa-brands fa-instagram"/>
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
    img {
        width: 100px;
        height: 40px;
    }
    .fa-chevron-down {
        display: inline-block;
    }
    * {
        font-size: 12px;
    }
</style>