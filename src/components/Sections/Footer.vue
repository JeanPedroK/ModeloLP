<template>
    <div class="copyright bg-gray">
        <div class="container">
            <div class="row">
                <div class="col-lg-6 col-md-12 col-sm-12">
                    <ul class="list-unstyled li-space-lg p-small">
                        <li><a href="#">Article Details</a></li>
                        <li><a href="#">Terms & Conditions</a></li>
                        <li><a href="#">Privacy Policy</a></li>
                    </ul>
                </div>
                <div class="col-lg-3 col-md-12 col-sm-12">
                    <p class="p-small statement">Copyright © <a href="#"></a></p>
                </div>
                <div class="col-lg-3 col-md-12 col-sm-12">
                    <p class="p-small statement">Distributed by <a href="#" target="_blank">
                        </a></p>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.copyright {
    padding-top: 1.5rem;
    border-top: 1px solid #d0dae2;
    text-align: center;
}

.copyright a {
    text-decoration: none;
}

.copyright .list-unstyled,
.copyright .statement {
    opacity: 0.7;
}
</style>
