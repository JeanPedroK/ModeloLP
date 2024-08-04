<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>

<template>
  <header class="header" id="homePage">
    <div class="container">
      <div class="row">
        <div class="col-lg-6 col-xl-5">
          <div class="text-container">
            <h1 class="h1-large">{{ msg }}</h1>
            <p class="p-large"> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut dignissim, neque ut ultrices
              sollicitudin Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut dignissim, neque ut ultrices
              sollicitudin</p>
            <!-- <a class="btn-solid-lg" href="#services">Serviços</a> -->
          </div>
        </div>
        <div class="col-lg-6 col-xl-7">
          <div class="image-container">
            <img class="img-fluid" src="/assets/images/header-image.png" alt="alternative" />
          </div>
        </div>
      </div>
      <div class="row" style="padding-top: 24rem;">
        <div class="basic-2">
          <div class="container">
            <div class="row">
              <div class="col-lg-6 col-xl-5">
                <div class="text-container">
                  <div class="section-title">ABOUT US</div>
                  <h2>We have ten years experience in marketing</h2>
                  <p>Etiam tempus condimentum congue. In sit amet nisi eget massa condimentum lobortis eget ac eros. In
                    hac habitasse platea dictumst. Aenean molestie mauris eget sapien sagittis, a bibendum magna
                    tincidunt
                  </p>
                </div>
              </div>
              <div class="col-lg-6 col-xl-7">
                <div class="image-container">
                  <img class="img-fluid" src="/assets/images/details-2.png" alt="alternative" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<style scoped lang="scss">
.header {
  background: url('/assets/images/header-background.jpg') center center no-repeat;
  background-size: cover;
  text-align: center;
  overflow: hidden;
  padding-top: 20.25rem;
  // padding-bottom: 20.3%;

  & .image-container {
    position: relative;

    & img {
      position: absolute;
      bottom: -450px;
      left: 60px;
      max-width: none;

    }
  }

  & .h1-large {
    margin-bottom: 1.75rem;
    font-size: 3.25rem;
    line-height: 3.75rem;
    font-weight: 700;
    text-align: left;
  }

  & .p-large {
    margin-bottom: 2.25rem;
    font-size: 1.125rem;
    line-height: 1.75rem;
    color: #5e6576;
    text-align: left;
  }

  & .image-container {
    margin-top: 5rem;
  }
}

.basic-2 {
  padding-top: 4.5rem;
  padding-bottom: 9.5rem;
  background: url('/assets/images/details-2-background.jpg') center center no-repeat;
  background-size: cover;

  & .text-container {
    margin-bottom: 4rem;
  }

  & h2 {
    margin-bottom: 1.75rem;
  }

  & p {
    margin-bottom: 2rem;
  }
}

@media screen and (max-width:500px) {
  .header {
    padding-top: 8rem;
    padding-bottom: 4em;

    & .image-container img {
      position: unset;
      bottom: unset;
      left: unset;
      max-width: 100%;
    }

    & .h1-large {
      text-align: center !important;
      font-size: 2.5rem !important;
      line-height: 3.25rem !important;
      letter-spacing: -0.4px;
    }

    & .p-large {
      text-align: center !important;
    }
  }

}
</style>
