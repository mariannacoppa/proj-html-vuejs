<script>
import contactInfos from '../../contact-infos.json'
import infoLinks from '../../info-links.json'
import FooterInfoItem from './FooterInfoItem.vue'
import FooterContItem from './FooterContItem.vue'
export default {
    components: {
        FooterContItem,
        FooterInfoItem
    },
    data () {
        return {
            infoObjs: contactInfos,
            linkObjs: infoLinks
        }
    }
}
</script>
<template>
    <footer class="container">
        <div class="row">
            <div class="col-3">
                <div class="contact">
                    h4.
                    <ul class="list-unstyled">
                        <FooterContItem v-for="(infoObj, index) in infoObjs" :icon="infoObj.icon" :info="infoObj.info" />
                    </ul>
                </div>
                <div class="info">
                    <ul class="list-unstyled">
                        <FooterInfoItem v-for="(linkObj, index) in linkObjs" :link="linkObj.link" />
                    </ul>
                </div>
                <div class="useful">
                    
                </div>
                <div class="news"></div>
            </div>
        </div>
    </footer>
</template>
<style lang="scss" scoped>
    
</style>