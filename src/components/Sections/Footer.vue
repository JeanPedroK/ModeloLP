<template>
    <div class="copyright bg-gray">
        <div class="container">
            <div class="row">
                <div class="col-lg-6 col-md-12 col-sm-12">
                    <ul class="list-unstyled li-space-lg p-small">
                        <li><a class="text-muted" href="#">Article Details</a></li>
                        <li><a class="text-muted" href="#">Terms & Conditions</a></li>
                        <li><a class="text-muted" href="#">Privacy Policy</a></li>
                    </ul>
                </div>
                <div class="col-lg-3 col-md-12 col-sm-12">
                    <p class="p-small statement">Copyright © <a class="nameCp" href="https://github.com/JeanPedroK"
                            target="_blank">JP</a></p>
                </div>
                <div class="col-lg-3 col-md-12 col-sm-12">
                    <p class="p-small statement">Distributed by <a href="#" class="nameCp" target="_blank">Name
                        </a></p>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.copyright {
    padding-top: 1rem;
    border-top: 1px solid #d0dae2;
    text-align: left;

    & a {
        text-decoration: none;
    }

    & .list-unstyled {
        opacity: 0.7;

        & li {
            display: inline-block;
            margin-right: 1rem;
        }
    }

    & .statement {
        opacity: 0.7;
        text-align: right;

    }

    & .nameCp {
        color: rgba(0, 189, 31, 0.706);
        cursor: pointer;
        font-weight: bold;
    }
}

@media screen and (max-width: 500px) {
    .copyright {
        & .list-unstyled {
            text-align: center;
        }

        & .statement {
            text-align: center;

        }

    }
}
</style>
