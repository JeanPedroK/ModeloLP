<template>
    <div class="cards-2 bg-gray">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <h2 class="h2-heading">Comentários</h2>
                </div>
            </div>
            <div class="row">
                <div class="col-lg-12 d-flex main-card">

                    <div class="card" v-for="(item, index) in testimonial" :key="index">
                        <img class="quotes" src="/assets/images/quotes.svg" alt="alternative" />
                        <div class="card-body">
                            <p class="testimonial-text">{{ item.content }}</p>
                            <div class="testimonial-author">{{ item.user }}</div>
                            <div class="occupation">{{ item.function }}</div>
                        </div>
                        <div class="gradient-floor red-to-blue"></div>
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
            testimonial: [
                { user: 'Roe Smith', function: 'General Manager, Presentop', content: 'Mauris ornare libero et pharetra hendrerit. Cura elementum lectus quis tellus pretium, vitae lobortis dui sagittis aliquam et enim vel semon anticus' },
                { user: 'Sam Bloom', function: 'General Manager, Presentop', content: 'Mauris ornare libero et pharetra hendrerit. Cura elementum lectus quis tellus pretium, vitae lobortis dui sagittis aliquam et enim vel semon anticus' },
                { user: 'Bill McKenzie', function: 'General Manager, Presentop', content: 'Mauris ornare libero et pharetra hendrerit. Cura elementum lectus quis tellus pretium, vitae lobortis dui sagittis aliquam et enim vel semon anticus' },
                { user: 'Vanya Dropper', function: 'General Manager, Presentop', content: 'Mauris ornare libero et pharetra hendrerit. Cura elementum lectus quis tellus pretium, vitae lobortis dui sagittis aliquam et enim vel semon anticus' },
                { user: 'Lefty Brown', function: 'General Manager, Presentop', content: 'Mauris ornare libero et pharetra hendrerit. Cura elementum lectus quis tellus pretium, vitae lobortis dui sagittis aliquam et enim vel semon anticus' },
                { user: 'Susane Blake', function: 'General Manager, Presentop', content: 'Mauris ornare libero et pharetra hendrerit. Cura elementum lectus quis tellus pretium, vitae lobortis dui sagittis aliquam et enim vel semon anticus' }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
.cards-2 {
    padding-top: 9.5rem;
    padding-bottom: 2.25rem;
    text-align: center;

    & .h2-heading {
        margin-bottom: 3.75rem;
    }

    & .main-card {
        flex-wrap: wrap;
        gap: 30px;
    }

    & .card {
        position: relative;
        margin-bottom: 5rem;
        border-radius: 10px;
        width: 400px;
        box-shadow: 0 4px 20px -1px rgba(0, 0, 0, 0.1);

        & .gradient-floor {
            position: absolute;
            bottom: 0;
            left: 0;
            height: 10px;
            width: 100%;
            border-bottom-left-radius: 10px;
            border-bottom-right-radius: 10px;
        }

        & .gradient-floor.red-to-blue {
            background: linear-gradient(to right, #ef3d91, #0092ff);
        }

        & .gradient-floor.blue-to-purple {
            background: linear-gradient(to right, #0092ff, #637eff);
        }

        & .gradient-floor.purple-to-green {
            background: linear-gradient(to right, #637eff, #16c66d);
        }
    }

    & .card .quotes {
        position: absolute;
        top: -15px;
        right: 0;
        left: 0;
        width: 48px;
        margin-right: auto;
        margin-left: auto;
    }

    & .card-body {
        padding: 3.5rem 2rem 3.125rem 2rem;
    }

    & .testimonial-author {
        margin-bottom: 0.125rem;
        color: #223150;
        font-weight: bold;
    }

    & .occupation {
        font-size: 0.875rem;
        line-height: 1.5rem;
    }
}

@media screen and (max-width: 500px) {
    .main-card {
        justify-content: center !important;
        gap: 5px !important;
    }
}
</style>