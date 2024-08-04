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
                                <i class="fas fa-circle fa-stack-2x"></i>
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
            social: [{ logo: 'fab fa-facebook-f fa-stack-1x', link: '#linkFace' },
            { logo: 'fab fa-twitter fa-stack-1x', link: '#linkX' },
            { logo: 'fab fa-pinterest-p fa-stack-1x', link: '#linkPint' },
            { logo: 'fab fa-instagram fa-stack-1x', link: '#linkInta' },
            { logo: 'fab fa-youtube fa-stack-1x', link: '#linkYoutube' },
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
}

.footer .decoration-circles {
	position: absolute;
	top: 96px;
	left: -60px;
}

.footer div[class*="col"] {  
	position: relative;
}

.footer a {
	color: #223150;
	text-decoration: none;
}

.footer h4 {
	margin-bottom: 1.875rem;
}

.footer .fa-stack {
	width: 2em;
	margin-bottom: 1.25rem;
	margin-right: 0.375rem;
	font-size: 1.5rem;
}

.footer .fa-stack .fa-stack-1x {
    color: hsla(130, 100%, 37%, 0.705);
	transition: all 0.2s ease;
}

.footer .fa-stack .fa-stack-2x {
	color: #ffffff;
	transition: all 0.2s ease;
}

.footer .fa-stack:hover .fa-stack-1x {
	color: #ffffff;
}

.footer .fa-stack:hover .fa-stack-2x {
    color: hsla(130, 100%, 37%, 0.705);
}
</style>