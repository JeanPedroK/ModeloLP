<template>
    <div class="slider-1">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <h4>Com a confiança de mais de <span
                            style="color: hsla(130, 100%, 37%, 0.705);font-weight: bold;">5000</span> clientes no mundo
                        todo!</h4>
                    <hr class="section-divider" />
                    <div class="slider-container">
                        <div class="swiper-container image-slider">
                            <div class="swiper-wrapper">
                                <div class="swiper-slide" v-for="(item, index) in logos" :key="index">
                                    <img class="img-fluid" :src="item.urlImg" alt="alternative" />
                                </div>
                            </div>
                        </div>
                    </div>

                </div>
            </div>
        </div>
    </div>
</template>

<script setup>

import { ref, onMounted, onBeforeUnmount } from 'vue';

var logos = [
    { urlImg: '/assets/images/customer-logo-1.png' },
    { urlImg: '/assets/images/customer-logo-2.png' },
    { urlImg: '/assets/images/customer-logo-3.png' },
    { urlImg: '/assets/images/customer-logo-4.png' },
    { urlImg: '/assets/images/customer-logo-5.png' },
    { urlImg: '/assets/images/customer-logo-6.png' },

]

onMounted(() => {
    var cardSlider = new Swiper('.card-slider', {
        autoplay: {
            delay: 4000,
            disableOnInteraction: false
        },
        loop: true,
        navigation: {
            nextEl: '.swiper-button-next',
            prevEl: '.swiper-button-prev'
        }
    });

    var imageSlider = new Swiper('.image-slider', {
        autoplay: {
            delay: 3000,
            disableOnInteraction: false
        },
        loop: true,
        spaceBetween: 50,
        slidesPerView: 5,
        breakpoints: {
            575: {
                slidesPerView: 1,
                spaceBetween: 10
            },
            767: {
                slidesPerView: 2,
                spaceBetween: 20
            },
            991: {
                slidesPerView: 3,
                spaceBetween: 20
            },
            1199: {
                slidesPerView: 4,
                spaceBetween: 20
            },

        }
    });


});

</script>

<style scoped lang="scss">
.slider-1 {
    padding-top: 2rem;
    padding-bottom: 3.75rem;
    background: linear-gradient(rgb(252, 250, 251), rgb(255, 255, 255));
    text-align: center;

    & h4 {
        margin-bottom: 0.25rem;
    }

    & .section-divider {
        margin-bottom: 1rem;
    }

    & .slider-container {
        margin-bottom: 0.5rem;
        padding: 1rem 0;
    }
}
</style>