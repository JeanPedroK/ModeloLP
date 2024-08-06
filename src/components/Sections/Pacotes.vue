<template>
    <div id="Prices" class="cards-1">
        <div class="container">
            <div class="row">
                <div class="col-lg-12 d-flex card-main">

                    <div class="card col align-items-center" v-for="(item, index) in pacotes" :key="index">
                        <div class="card-icon">
                            <span :class="item.iconPacote + item.iconColor"></span>
                        </div>
                        <div class="card-body">
                            <h5 class="card-title">{{ item.tituloPacote }}</h5>
                            <span>
                                <i v-for="i in item.estrelas" :key="i" class="fas fa-star iconYellow"></i>
                                <i v-for="i in (5 - item.estrelas)" :key="i" class="far fa-star"></i>
                            </span>
                            <div aria-hidden="true">{{ item.avaliacoes }}</div>
                            <div class="d-flex">
                                <ul class="d-flex flex-row" style="gap:5px;">
                                    <li class="text-muted">{{ item.compativeis }}</li>
                                </ul>
                            </div>
                            <ul class="d-flex">
                                <li class="d-flex">
                                    <i class="fas fa-solid fa-check icon-check"></i>
                                    <p>{{ item.info1 }}</p>
                                </li>
                                <li class="d-flex">
                                    <i class="fas fa-solid fa-check icon-check"></i>
                                    <p>{{ item.info2 }}</p>

                                </li>
                                <li class="d-flex">
                                    <i class="fas fa-solid fa-check icon-check"></i>
                                    <p>{{ item.info3 }}</p>

                                </li>
                                <li class="d-flex">
                                    <i class="fas fa-solid fa-check icon-check"></i>
                                    <p>{{ item.info4 }}</p>

                                </li>
                            </ul>

                        </div>
                        <button class="buyButton btn btn-success" type="button">
                            <a class="read-more no-line" type="button" href="#">Assinar<span
                                    class="fas fa-solid fa-pen-nib"></span></a>
                        </button>
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
            pacotes: [
                { tituloPacote: 'Pacote Básico', iconPacote: 'fas fa-fish', iconColor: ' green', info1: 'Et blandit nisl libero at arcu. Donec ac lectus sed tellus mollis viverra.', info2: 'Et blandit nisl libero at arcu. Donec ac lectus sed tellus mollis viverra.', info3: 'Et blandit nisl libero at arcu. Donec ac lectus sed tellus mollis viverra.', info4: 'Et blandit nisl libero at arcu. Donec ac lectus sed tellus mollis viverra.', compativeis: 'Windows® macOS® Android™ iOS®', avaliacoes: '(8 avaliações)', estrelas: 3 },
                { tituloPacote: 'Pacote Intermediário', iconPacote: 'fas fa-horse', iconColor: ' blue', info1: 'Et blandit nisl libero at arcu. Donec ac lectus sed tellus mollis viverra.', info2: 'Et blandit nisl libero at arcu. Donec ac lectus sed tellus mollis viverra.', info3: 'Et blandit nisl libero at arcu. Donec ac lectus sed tellus mollis viverra.', info4: 'Et blandit nisl libero at arcu. Donec ac lectus sed tellus mollis viverra.', compativeis: 'Windows® macOS® Android™ iOS®', avaliacoes: '(868 avaliações)', estrelas: 4 },
                { tituloPacote: 'Pacote Avançado', iconPacote: 'fas fa-dragon', iconColor: ' red', info1: 'Et blandit nisl libero at arcu. Donec ac lectus sed tellus mollis viverra.', info2: 'Et blandit nisl libero at arcu. Donec ac lectus sed tellus mollis viverra.', info3: 'Et blandit nisl libero at arcu. Donec ac lectus sed tellus mollis viverra.', info4: 'Et blandit nisl libero at arcu. Donec ac lectus sed tellus mollis viverra.', compativeis: 'Windows® macOS® Android™ iOS®', avaliacoes: '(118 avaliações)', estrelas: 5 },
            ]
        }
    }
}


</script>
<style scoped lang="scss">
ul {
    list-style-type: none;
    padding-left: 10px;
    padding-top: 5px;
    flex-direction: column;

    & li {
        flex-direction: row;
        gap: 10px;
    }
}

.iconYellow {
    color: #ffe810;
}

.icon-check {
    padding-top: 5px;
    color: rgb(0, 168, 142);
    ;
}

.container {
    padding-top: 7rem;
}

.cards-1 {
    padding-bottom: 2.25em;

    & h2 {
        margin-bottom: 3.5rem;
        color: #223150;
        font-weight: 700;
        font-size: 2rem;
        line-height: 2.5rem;
        letter-spacing: -0.4px;
    }

    & .card {
        margin-bottom: 2.5rem;
        border: none;
        background-color: transparent;
        box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
        padding: 25px;
        transition: all 0.4s;

        &:hover {
            transform: scale(1.05);
        }
    }

    & .card-icon {
        width: 66px;
        height: 66px;
        margin-bottom: 1.875rem;
        border-radius: 8px;
        background-color: #ddedfb;
        text-align: center;

    }

    & .card-body {
        padding: 0;
        display: contents;

        & p {
            margin-bottom: 1.125rem;
        }
    }

    & .card-title {
        margin-bottom: .4rem;
    }

    & .read-more {
        color: white;
        font-weight: 700;
        font-weight: bold;
        font-size: 1.2rem;
        line-height: 1.5rem;
        text-decoration: none;

        & .fas {
            color: white;
            margin-left: 0.625rem;
            font-size: 1rem;
            vertical-align: -8%;
        }

    }

    & .card-main {
        gap: 20px;
        flex-direction: row;
    }
}


.red {
    color: #ef473d !important;
}

.green {
    color: #16c66d;
}

.blue {
    color: #0092ff;
}

.cards-1 .card-icon .fas,
.cards-1 .card-icon .far {
    font-size: 2rem;
    line-height: 66px;
}

@media screen and (max-width: 500px) {
    .container {
        padding-top: 3rem;
    }

    .cards-1 {
        padding-top: 5rem;

        & .card-main {
            gap: 5px;
            flex-direction: column;
        }

        & .card {
            margin-bottom: 2rem;
        }
    }
}
</style>