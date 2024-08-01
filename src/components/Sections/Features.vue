<template>
    <div id="features" class="accordion-1">
        <div class="container">
            <div class="row">
                <div class="col-xl-12">
                    <h2 class="h2-heading">Online service features</h2>
                    <p class="p-heading">Suspendisse vitae enim arcu. Aliquam convallis risus a felis blandit, at mollis
                        nisi bibendum. Aliquam nec purus at ex blandit posuere nec a odio. Proin lacinia dolor justo</p>
                </div>
            </div>
            <div class="row">
                <div class="col-xl-5">
                    <div class="accordion" id="accordionExample">


                        <div class="accordion-item">
                            <div class="accordion-icon">
                                <span class="fas fa-tv"></span>
                            </div>
                            <div class="accordion-header" id="headingOne">
                                <button class="accordion-button" type="button" data-bs-toggle="collapse"
                                    data-bs-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                                    Planejamento
                                </button>
                            </div>
                            <div id="collapseOne" class="accordion-collapse collapse show" aria-labelledby="headingOne"
                                data-bs-parent="#accordionExample">
                                <div class="accordion-body">Mauris ornare libero et pharetra hendrerit. Cura elementum
                                    lectus quis tellus pretium, vitae lobortis dui sagittis aliquam et enim vel semon
                                    anticus</div>
                            </div>
                        </div>


                        <div class="accordion-item">
                            <div class="accordion-icon blue">
                                <span class="fas fa-microphone"></span>
                            </div>
                            <div class="accordion-header" id="headingTwo">
                                <button class="accordion-button" type="button" data-bs-toggle="collapse"
                                    data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                                    Oportunidades
                                </button>
                            </div>
                            <div id="collapseTwo" class="accordion-collapse collapse" aria-labelledby="headingTwo"
                                data-bs-parent="#accordionExample">
                                <div class="accordion-body">Mauris ornare libero et pharetra hendrerit. Cura elementum
                                    lectus quis tellus pretium, vitae lobortis dui sagittis aliquam et enim vel semon
                                    anticus</div>
                            </div>
                        </div>


                        <div class="accordion-item">
                            <div class="accordion-icon purple">
                                <span class="fas fa-video"></span>
                            </div>
                            <div class="accordion-header" id="headingThree">
                                <button class="accordion-button" type="button" data-bs-toggle="collapse"
                                    data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                                    Campanha
                                </button>
                            </div>
                            <div id="collapseThree" class="accordion-collapse collapse" aria-labelledby="headingThree"
                                data-bs-parent="#accordionExample">
                                <div class="accordion-body">Mauris ornare libero et pharetra hendrerit. Cura elementum
                                    lectus quis tellus pretium, vitae lobortis dui sagittis aliquam et enim vel semon
                                    anticus</div>
                            </div>
                        </div>


                        <div class="accordion-item">
                            <div class="accordion-icon orange">
                                <span class="fas fa-tools"></span>
                            </div>
                            <div class="accordion-header" id="headingFour">
                                <button class="accordion-button" type="button" data-bs-toggle="collapse"
                                    data-bs-target="#collapseFour" aria-expanded="false" aria-controls="collapseFour">
                                    Ajustes
                                </button>
                            </div>
                            <div id="collapseFour" class="accordion-collapse collapse" aria-labelledby="headingFour"
                                data-bs-parent="#accordionExample">
                                <div class="accordion-body">Mauris ornare libero et pharetra hendrerit. Cura elementum
                                    lectus quis tellus pretium, vitae lobortis dui sagittis aliquam et enim vel semon
                                    anticus</div>
                            </div>
                        </div>

                    </div>
                </div>
                <div class="col-xl-7 d-flex flex-row-reverse">
                    <div class="image-container">
                        <img class="img-fluid" src="/assets/images/features-dashboard.png" alt="alternative" />
                    </div>
                </div>
                
            </div>
        </div>
    </div>
</template>

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
    transition: all 0.4s;

    & img:hover {
        transform: scale(1.15);
        transition: all 0.4s;
    }
}

.accordion-1 {
    padding-top: 9.25rem;
    padding-bottom: 9.75rem;
    background: url('/assets/images/features_backgroud.jpg') center center no-repeat;
    background-size: cover;
}

.accordion-1 .h2-heading {
    margin-bottom: 1rem;
    // color: #ffffff;
    text-align: center;
    padding-top: 6px;
    font-weight: 600px;
}

.accordion-1 .p-heading {
    margin-bottom: 4rem;
    // color: #ffffff;
    text-align: center;
}

.accordion-1 .accordion {
    margin-bottom: 5rem;
}

.accordion-1 .accordion-item {
    margin-bottom: 2.5rem;
    border: none;
    border-radius: 0;
    background-color: transparent;
}

.accordion-1 .accordion-item:last-of-type {
    margin-bottom: 0;
}

.accordion-1 .accordion-icon {
    position: absolute;
    width: 44px;
    height: 44px;
    border-radius: 4px;
    text-align: center;
    background-color: #14be9f;
}

.accordion-1 .accordion-icon.blue {
    background-color: #1d79fb;
}

.accordion-1 .accordion-icon.purple {
    background-color: #dc63ff;
}

.accordion-1 .accordion-icon.orange {
    background-color: #ff6c02;
}

.accordion-1 .accordion-icon .fas {
    // color: #ffffff;
    font-size: 1.25rem;
    line-height: 44px;
}

.accordion-1 .accordion-header {
    margin-left: 4.125rem;
    padding: 0.5rem 0 0.5rem 0;
    border: none;
    background-color: transparent;
}

.accordion-1 .accordion-header button {
    padding: 0;
    border: none;
    background-color: transparent;
    // color: #ffffff;
    box-shadow: none;
    font-weight: 700;
    font-size: 1.25rem;
    line-height: 1.625rem;
    letter-spacing: -0.4px;
    text-align: left;
}

.accordion-1 .accordion-header button:after {
    display: none;
}

.accordion-1 .accordion-body {
    margin-left: 4.125rem;
    padding: 0.375rem 0 0 0;
    // color: #ffffff;
}
</style>