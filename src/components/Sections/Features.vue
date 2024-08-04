<template>
    <div id="features" class="accordion-1">
        <div class="container">
            <div class="row">
                <div class="col-xl-12">
                    <h2 class="h2-heading">Features</h2>
                    <p class="p-heading">Suspendisse vitae enim arcu. Aliquam convallis risus a felis blandit, at mollis
                        nisi bibendum. Aliquam nec purus at ex blandit posuere nec a odio. Proin lacinia dolor justo</p>
                </div>
            </div>
            <div class="row">
                <div class="col-xl-5">
                    <div v-for="(item, index) in items" :key="index" class="accordion-item">
                        <div class="accordion-icon" :class="item.iconColor">
                            <span :class="item.iconClass"></span>
                        </div>
                        <div class="accordion-header" :id="'heading' + index">
                            <button class="accordion-button" type="button" @click="userToggle(index)"
                                :aria-expanded="activeIndex === index" :aria-controls="'collapse' + index">
                                {{ item.title }}
                            </button>
                        </div>
                        <transition name="fade">
                            <div :id="'collapse' + index" class="accordion-collapse collapse"
                                :class="{ show: activeIndex === index }" :aria-labelledby="'heading' + index">
                                <div class="accordion-body">
                                    {{ item.content }}
                                </div>
                            </div>
                        </transition>
                    </div>
                </div>
                <div class="col-xl-7 d-flex flex-row-reverse">
                    <div class="image-container" id="imgBox" @mousemove="handleMouseMove"
                        @mouseleave="handleMouseLeave">
                        <img class="responsive-img" src="/assets/images/features-dashboard.png" ref="img"
                            alt="alternative" />
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
            activeIndex: 0,
            intervalId: null,
            pauseDuration: 5000,
            items: [
                { title: 'Planejamento', iconClass: 'fas fa-tv', iconColor: '', content: 'Mauris ornare libero et pharetra hendrerit. Cura elementum lectus quis tellus pretium, vitae lobortis dui sagittis aliquam et enim vel semon anticus' },
                { title: 'Oportunidades', iconClass: 'fas fa-microphone', iconColor: 'blue', content: 'Mauris ornare libero et pharetra hendrerit. Cura elementum lectus quis tellus pretium, vitae lobortis dui sagittis aliquam et enim vel semon anticus' },
                { title: 'Campanha', iconClass: 'fas fa-video', iconColor: 'purple', content: 'Mauris ornare libero et pharetra hendrerit. Cura elementum lectus quis tellus pretium, vitae lobortis dui sagittis aliquam et enim vel semon anticus' },
                { title: 'Ajustes', iconClass: 'fas fa-tools', iconColor: 'orange', content: 'Mauris ornare libero et pharetra hendrerit. Cura elementum lectus quis tellus pretium, vitae lobortis dui sagittis aliquam et enim vel semon anticus' }
            ]
        };
    },
    methods: {
        // img zoom
        handleMouseMove(event) {
            const box = event.currentTarget;
            const img = this.$refs.img;

            const rect = box.getBoundingClientRect();
            const x = event.clientX - rect.left;
            const y = event.clientY - rect.top;

            img.style.transformOrigin = `${x}px ${y}px`;
            img.style.transform = 'scale(1.5)';
        },
        handleMouseLeave() {
            const img = this.$refs.img;
            img.style.transformOrigin = 'center center';
            img.style.transform = 'scale(1)';
        },

        // accordions
        toggle(index) {
            this.activeIndex = this.activeIndex === index ? null : index;
        },
        autoToggle() {
            this.intervalId = setInterval(() => {
                this.activeIndex = (this.activeIndex + 1) % this.items.length;
            }, 3000);
        },
        userToggle(index) {
            clearInterval(this.intervalId);
            this.toggle(index);
            setTimeout(() => {
                this.autoToggle();
            }, this.pauseDuration);
        }
    },
    mounted() {
        this.autoToggle();
    }
};
</script>

<style scoped lang="scss">
.container {
    background-color: rgb(233 236 239 / 94%);
    padding-left: 50px;
    padding-right: 50px;
    padding-top: 20px;
    padding-bottom: 20px;
    border-radius: 10px;
}

.image-container {
    overflow: hidden;
    position: relative;
}

.responsive-img {
    transition: transform 0.3s ease;
}

.accordion-1 {
    padding-top: 12.25rem;
    padding-bottom: 12.75rem;
    background: url('/assets/images/features_backgroud.jpg') center center no-repeat;
    background-size: cover;

    & .h2-heading {
        margin-bottom: 1rem;
        text-align: center;
        padding-top: 6px;
        font-weight: 600px;
    }

    & .p-heading {
        margin-bottom: 4rem;
        text-align: center;
    }

    & .accordion {
        margin-bottom: 5rem;
    }

    & .accordion-item {
        margin-bottom: 2.5rem;
        border: none;
        border-radius: 0;
        background-color: transparent;
    }

    & .accordion-item:last-of-type {
        margin-bottom: 0;
    }

    & .accordion-icon {
        position: absolute;
        width: 44px;
        height: 44px;
        border-radius: 4px;
        text-align: center;
        background-color: #14be9f;
    }

    & .accordion-icon.blue {
        background-color: #1d79fb;
    }

    & .accordion-icon.purple {
        background-color: #dc63ff;
    }

    & .accordion-icon.orange {
        background-color: #ff6c02;
    }

    & .accordion-icon .fas {
        color: #ffffff;
        font-size: 1.25rem;
        line-height: 44px;
    }

    & .accordion-header {
        margin-left: 4.125rem;
        padding: 0.5rem 0 0.5rem 0;
        border: none;
        background-color: transparent;
    }

    & .accordion-header button {
        padding: 0;
        border: none;
        background-color: transparent;
        box-shadow: none;
        font-weight: 700;
        font-size: 1.25rem;
        line-height: 1.625rem;
        letter-spacing: -0.4px;
        text-align: left;
    }

    & .accordion-header button:after {
        display: none;
    }
}

.fade-enter-active {
    transition: all 0.5s ease-out;
}

.fade-leave-active {
    transition: all 0.5s ease-out;
}

.fade-enter-from,
.fade-leave-to {
    transform: translateY(-100%);
    opacity: 0;
}
</style>