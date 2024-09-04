<script>
import contactInfos from '../../contact-infos.json'
import infoLinks from '../../info-links.json'
import usefulLinks from '../../useful-links.json'
import FooterInfoItem from './FooterInfoItem.vue'
import FooterContItem from './FooterContItem.vue'
import UsefulLink from './UsefulLink.vue'
export default {
    components: {
        FooterContItem,
        FooterInfoItem,
        UsefulLink
    },
    data () {
        return {
            infoObjs: contactInfos,
            linkObjs: infoLinks,
            useLinkObjs: usefulLinks
        }
    }
}
</script>
<template>
    <div class="bg-black">
        <footer class="container">
            <div class="row">
                <div class="col-3 py-5">
                    <div class="contact">
                        <h4 class="footer-title text-white">
                            CONTACT INFO
                        </h4>
                        <ul class="list-unstyled">
                            <FooterContItem v-for="(infoObj, index) in infoObjs" :icon="infoObj.class" :info="infoObj.info" />
                        </ul>
                    </div>  
                </div>
                <div class="col-3 py-5">
                    <div class="info">
                        <h4 class="footer-title text-white">
                            INFORMATION
                        </h4>
                        <ul class="list-unstyled">
                            <FooterInfoItem v-for="(linkObj, index) in linkObjs" :link="linkObj.link" />
                        </ul>
                    </div>              
                </div>
                <div class="col-3 py-5">
                    <div class="useful">
                        <h4 class="footer-title text-white">
                            USEFUL LINKS
                        </h4>
                        <ul class="list-unstyled">
                            <UsefulLink v-for="(useLinkObj, index) in useLinkObjs" :link="useLinkObj.link" />
                        </ul>
                    </div>
                </div>
                <div class="col-3 py-5">
                    <div class="news">
                        <h4 class="footer-title text-white">
                            NEWSLETTER
                        </h4>
                        <p class="mb-2">Subscribe to receive Inspiration, Ideas & News in Your Inbox.</p>
                        <input type="text" placeholder="Enter Your Email"><br>
                        <button class="btn btn-light mt-3">SUBSCRIBE</button>
                    </div>
                </div>
            </div>
            <hr>
            <div class="text-center footer-bottom pb-4 pt-2"><i class="fa-regular fa-copyright"></i> 2023 All Rights Reserved. Developed by TemplateMela</div>
        </footer>
    </div>
</template>
<style lang="scss" scoped>
footer {
    background-color: black;
    ul, .text-center, p {
        color: rgb(179, 174, 174);
    }
    .footer-bottom, .news, .info, .useful, .contact {
        font-size: 12px;
    }
    h4 {
        font-size: 15px;
    }
    hr {
        height: 2px;
        color: #f2f2f2;
    }
    input {
        background-color: #1D1C1B;
        border: none;
    }
}
</style>