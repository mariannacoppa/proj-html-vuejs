<script>
import NavMenuItems from '../../navMenuItems.json';
import NavIconItems from '../../navIconItems.json';
import NavMenuItem from './NavMenuItem.vue';
import NavIconItem from './NavIconItem.vue';
export default {
    components: {
        NavMenuItem,
        NavIconItem
    },
    data () {
        return {
            navobjs: NavMenuItems,
            iconObjs: NavIconItems
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
                    <div class="icons d-flex">
                        <i class="fa-solid fa-magnifying-glass"/>
                        <span class="brands d-flex">
                            <NavIconItem class="me-2" v-for="(iconObj, index) in iconObjs" :class="iconObj.class" />
                        </span>
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

</style>