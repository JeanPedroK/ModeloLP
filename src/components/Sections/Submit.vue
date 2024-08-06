<template>
    <div id="contact" class="form-1">
        <div class="container">
            <div class="row">
                <div class="col-lg-6">
                    <div class="text-container">
                        <div class="section-title"></div>
                        <h2 class="text-center">Entre em contato</h2>
                        <p>Aliquam et enim vel sem pulvinar suscipit sit amet quis lorem. Sed risus ipsum, egestas sed
                            odio in, pulvinar euismod ipsum. Sed ut enim non nunc fermentum dictum et sit amet erat.
                        </p>
                    </div>
                </div>
                <div class="col-lg-6">

                    <form>
                        <div class="form-group" v-for="(item, index) in dataSubmit" :key="index">
                            <input :type="item.text" class="form-control-input" :placeholder="item.name" required />
                        </div>
                    </form>
                    <div class="form-group">
                        <button type="submit" class="form-control-submit-button">Submit</button>
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
            dataSubmit: [{ name: 'Nome', type: 'text', },
            { name: 'Email', type: 'email', },
            { name: 'Empresa', type: 'text', },
            { name: 'Produto', type: 'text', },
            ]
        }
    }
}

</script>

<style scoped lang="scss">
.form-1 {
    padding-top: 9.5rem;
    padding-bottom: 8.75rem;

    & .text-container {
        margin-bottom: 4rem;
        text-align: center;
    }

    & .section-divider {
        margin-bottom: 1rem;
    }

    & h2 {
        margin-bottom: 1.75rem;
    }

    & .list-unstyled {
        & .fas {
            font-size: 0.375rem;
            line-height: 1.625rem;
        }

        & .flex-grow-1 {
            margin-left: 0.5rem;
        }
    }
}

.form-control-submit-button {
    display: inline-block;
    width: 100%;
    height: 3.25rem;
    border: 1px solid rgba(0, 189, 31, 0.706);
    border-radius: 30px;
    background-color: rgba(0, 189, 31, 0.706);
    color: #ffffff;
    font-weight: 600;
    font-size: 0.875rem;
    line-height: 0;
    cursor: pointer;
    transition: all 0.2s;

    &:hover {
        border: 1px solid rgba(0, 189, 31, 0.706);
        background-color: transparent;
        color: rgba(0, 189, 31, 0.706);
    }

}

.form-group {
    position: relative;
    margin-bottom: 1.25rem;
}

.form-control-input,
.form-control-textarea {
    width: 100%;
    padding-top: 0.875rem;
    padding-bottom: 0.875rem;
    padding-left: 1.5rem;
    border: 1px solid #cbcbd1;
    border-radius: 8px;
    background-color: #ffffff;
    font-size: 0.875rem;
    line-height: 1.5rem;
    -webkit-appearance: none;
}

.form-control-textarea {
    display: block;
    height: 14rem;
}

.form-control-input:focus,
.form-control-textarea:focus {
    border: 1px solid #a1a1a1;
    outline: none;
}

.form-control-input:hover,
.form-control-textarea:hover {
    border: 1px solid #a1a1a1;
}
</style>