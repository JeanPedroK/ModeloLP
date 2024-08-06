<template>
    <div class="footer bg-gray">
        <img class="decoration-circles" src="/assets/images/decoration-circles.png" alt="alternative" />
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <h4>Follow us</h4>
                    <div class="social-container">
                        <span class="fa-stack" v-for="(item, index) in social" :key="index">
                            <a :href="item.link">
                                <i :class="item.logo"></i>
                            </a>
                        </span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    data() {
        return {
            social: [{ logo: 'fab fa-facebook fa-stack-1x faceBook', link: '#linkFace' },
            { logo: 'fab fa-twitter fa-stack-1x', link: '#linkX' },
            // { logo: 'fab fa-pinterest-p fa-stack-1x', link: '#linkPint' },
            { logo: 'fab fa-instagram fa-stack-1x instagram', link: '#linkInta' },
            { logo: 'fab fa-youtube fa-stack-1x youtube', link: '#linkYoutube' },
            ]
        }
    }
}

</script>

<style lang="scss" scoped>
.footer {
    position: relative;
    padding-top: 7.5rem;
    padding-bottom: 6rem;
    text-align: center;

    & .decoration-circles {
        position: absolute;
        top: 96px;
        left: -60px;
    }

    & a {
        text-decoration: none;
    }

    & h4 {
        margin-bottom: 1.875rem;
    }

    & .fa-stack {
        width: 2em;
        margin-bottom: 1.25rem;
        margin-right: 0.375rem;
        font-size: 1.5rem;

        & .fa-stack-1x.faceBook {
            color: #0866ff;
        }

        & .fa-stack-1x.instagram {
            color: #eb2e9c
        }

        & .fa-stack-1x.youtube {
            color: #fd0000
        }
    }

}

.footer .footer div[class*="col"] {
    position: relative;
}
</style>