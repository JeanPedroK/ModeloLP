<template>
    <nav id="navbarExample" class="navbar navbar-expand-lg fixed-top navbar-light" aria-label="Main navigation">
        <div class="container">

            <a class="navbar-brand logo-text" href="#homePage">MODELO LP</a>
            <button class="navbar-toggler p-0 border-0" type="button" id="navbarSideCollapse"
                @click="toggleMenu = !toggleMenu" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>

            <div class="navbar-collapse offcanvas-collapse" v-show="toggleMenu" id="navbarsExampleDefault">
                <ul class="navbar-nav ms-auto navbar-nav-scroll">
                    <li class="nav-item">
                        <a class="nav-link" aria-current="page" href="#homePage">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#services">Serviços</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#features">Features</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#prices">Pacotes</a>
                    </li>
                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle" href="#" id="dropdown01" data-bs-toggle="dropdown"
                            aria-expanded="false" @click="toggleDropdown" @mouseover="handleMouseOver">Sobre</a>

                        <ul class="dropdown-menu" aria-labelledby="dropdown01" :class="{ show: isOpen }"
                            @mouseleave="handleMouseLeave">
                            <li><a class="dropdown-item" href="#">Artigos</a></li>
                            <li>
                                <div class="dropdown-divider"></div>
                            </li>
                            <li><a class="dropdown-item" href="#">Termos e Condições</a></li>
                            <li>
                                <div class="dropdown-divider"></div>
                            </li>
                            <li><a class="dropdown-item" href="#">Politicas de Privacidade</a></li>
                        </ul>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<script>

export default {
    name: 'App',
    data() {
        return {
            toggleMenu: false,
            isOpen: false,
            timeout: null
        }
    },
    methods: {
        toggleDropdown(event) {
            event.preventDefault();
            event.stopPropagation();
            this.isOpen = !this.isOpen;
        },
        handleMouseOver() {
            if (this.timeout) clearTimeout(this.timeout);
            this.isOpen = true;
        },
        handleMouseLeave() {
            this.timeout = setTimeout(() => {
                this.isOpen = false;
            }, 200); // Delay to allow click events to register
        }
    }
}

</script>


<style scoped lang="scss">
@media screen and (max-width: 500px) {
    .navbar-nav {
        align-items: center;
        padding-top: 1rem;
    }

    .container {
        max-width: 100% !important;
    }
}

.container {
    max-width: 80%;
}

.navbar {
    background-color: #414141;
    font-weight: 600;
    font-size: 0.875rem;
    box-shadow: 0 1px 6px 0 rgba(0, 0, 0, 0.05);

    &-brand.logo-text {
        color: #fcfafb;
        font-weight: 700;
        font-size: 1.875rem;
        line-height: 1rem;
        text-decoration: none;
        padding-left: 1rem;

        &:hover {
            cursor: pointer;
            background-color: transparent;
            color: #fcfafb;
        }

        &:focus {
            color: #fcfafb;
        }
    }

    & .nav-item .nav-link {
        padding-top: 0.20rem;
        padding-right: 0.75rem;
        padding-left: 0.75rem;
        border-radius: 5px;
        font-size: 20px;
        color: #fcfafb;
        text-align: center;

        &:hover {
            background-color: hsla(130, 100%, 37%, 0.2);
            color: #fcfafb;
        }

        &:focus {
            color: #fcfafb;

        }
    }

    & .dropdown-menu {
        padding-top: 0.75rem;
        padding-bottom: 0.75rem;
        box-shadow: 0 3px 3px 1px rgba(0, 0, 0, 0.08);
        background-color: #414141;

        & .dropdown-item {
            color: #fcfafb;

        }

        & a:hover {
            background-color: hsla(130, 100%, 37%, 0.2);
            border-radius: 5px;
            color: #fcfafb;

        }

        &-divider {
            width: 90%;
        }

    }
}

.navbar .nav-item .nav-link .navbar .dropdown .dropdown-menu {
    animation: fadeDropdown 0.2s;
}

@keyframes fadeDropdown {
    0% {
        opacity: 0;
    }

    100% {
        opacity: 1;
    }
}
</style>