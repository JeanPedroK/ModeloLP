<template>
    <div id="contact" class="form-1">
        <div class="container">
            <div class="row">
                <div class="col-lg-6">
                    <div class="text-container">
                        <div class="section-title">GET QUOTE</div>
                        <h2>Submit the form for quote</h2>
                        <p>Aliquam et enim vel sem pulvinar suscipit sit amet quis lorem. Sed risus ipsum, egestas sed
                            odio in, pulvinar euismod ipsum. Sed ut enim non nunc fermentum dictum et sit amet erat.
                            Maecenas</p>
                        <ul class="list-unstyled li-space-lg">
                            <li class="d-flex">
                                <i class="fas fa-square"></i>
                                <div class="flex-grow-1">Vel maximus nunc aliquam ut. Donec semper, magna a pulvinar
                                </div>
                            </li>
                            <li class="d-flex">
                                <i class="fas fa-square"></i>
                                <div class="flex-grow-1">Suscipit sit amet quis lorem. Sed risus ipsum, egestas mare
                                </div>
                            </li>
                            <li class="d-flex">
                                <i class="fas fa-square"></i>
                                <div class="flex-grow-1">Sem pulvinar suscipit sit amet quis lorem. Sed risus</div>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="col-lg-6">

                    <form>
                        <div class="form-group">
                            <input type="text" class="form-control-input" placeholder="Name" required />
                        </div>
                        <div class="form-group">
                            <input type="email" class="form-control-input" placeholder="Email" required />
                        </div>
                        <div class="form-group">
                            <input type="text" class="form-control-input" placeholder="Industry" required />
                        </div>
                        <div class="form-group">
                            <input type="text" class="form-control-input" placeholder="Your product" required />
                        </div>
                        <div class="form-group">
                            <button type="submit" class="form-control-submit-button">Submit</button>
                        </div>
                    </form>

                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
.form-1 {
    padding-top: 9.5rem;
    padding-bottom: 8.75rem;
}

.form-1 .text-container {
    margin-bottom: 4rem;
}

.form-1 .section-divider {
    margin-bottom: 1rem;
}

.form-1 h2 {
    margin-bottom: 1.75rem;
}

.form-1 .list-unstyled .fas {
    font-size: 0.375rem;
    line-height: 1.625rem;
}

.form-1 .list-unstyled .flex-grow-1 {
    margin-left: 0.5rem;
}
</style>