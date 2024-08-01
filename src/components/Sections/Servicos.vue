<template>
  <div id="services" class="cards-1 bg-gray">
    <div class="container">
      <div class="row">
        <div class="col-lg-12">
          <h2 class="text-center" style="margin-top: 4rem;">Explore os serviços</h2>
        </div>
      </div>
      <div class="row">
        <div class="col-lg-12 d-flex card-main">

          <div class="card col align-items-center">
            <div class="card-icon">
              <span class="fas fa-headphones-alt"></span>
            </div>
            <div class="card-body">
              <h5 class="card-title">Análise de produtos</h5>
              <p>Et blandit nisl libero at arcu. Donec ac lectus sed tellus mollis viverra. Nullam pharetra ante at nunc
                elementum</p>
              <a class="read-more no-line" href="#">Learn more <span class="fas fa-long-arrow-alt-right"></span></a>
            </div>
          </div>

          <div class="card col align-items-center">
            <div class="card-icon red">
              <span class="far fa-clipboard"></span>
            </div>
            <div class="card-body">
              <h5 class="card-title">Oportunidades</h5>
              <p>Vulputate nibh feugiat. Morbi pellent diam nec libero lacinia, sed ultrices velit scelerisque. Nunc
                placerat justo sem</p>
              <a class="read-more no-line" href="#">Learn more <span class="fas fa-long-arrow-alt-right"></span></a>
            </div>
          </div>

          <div class="card col align-items-center">
            <div class="card-icon green">
              <span class="far fa-comments"></span>
            </div>
            <div class="card-body">
              <h5 class="card-title">Comunicação</h5>
              <p>Ety suscipit metus sollicitudin euqu isq imperdiet nibh nec magna tincidunt, nec pala vehicula neque
                sodales verum</p>
              <a class="read-more no-line" href="#">Learn more <span class="fas fa-long-arrow-alt-right"></span></a>
            </div>
          </div>
        </div>
        <div class="col-lg-12 d-flex card-main">

          <div class="card col align-items-center">
            <div class="card-icon">
              <span class="fas fa-headphones-alt"></span>
            </div>
            <div class="card-body">
              <h5 class="card-title">Análise de produtos</h5>
              <p>Et blandit nisl libero at arcu. Donec ac lectus sed tellus mollis viverra. Nullam pharetra ante at nunc
                elementum</p>
              <a class="read-more no-line" href="#">Learn more <span class="fas fa-long-arrow-alt-right"></span></a>
            </div>
          </div>

          <div class="card col align-items-center">
            <div class="card-icon red">
              <span class="far fa-clipboard"></span>
            </div>
            <div class="card-body">
              <h5 class="card-title">Oportunidades</h5>
              <p>Vulputate nibh feugiat. Morbi pellent diam nec libero lacinia, sed ultrices velit scelerisque. Nunc
                placerat justo sem</p>
              <a class="read-more no-line" href="#">Learn more <span class="fas fa-long-arrow-alt-right"></span></a>
            </div>
          </div>

          <div class="card col align-items-center">
            <div class="card-icon green">
              <span class="far fa-comments"></span>
            </div>
            <div class="card-body">
              <h5 class="card-title">Comunicação</h5>
              <p>Ety suscipit metus sollicitudin euqu isq imperdiet nibh nec magna tincidunt, nec pala vehicula neque
                sodales verum</p>
              <a class="read-more no-line" href="#">Learn more <span class="fas fa-long-arrow-alt-right"></span></a>
            </div>
          </div>



        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">

.container {
  padding-top: 3rem;
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
    margin-bottom: 1.125rem;
  }

  & .read-more {
    color: #223150;
    font-weight: 600;
    font-size: 0.875rem;
    line-height: 1.5rem;
    text-decoration: none;

    & .fas {
      color: #223150;
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

.cards-1 .card-icon .fas,
.cards-1 .card-icon .far {
  color: #0092ff;
  font-size: 2rem;
  line-height: 66px;
}

.cards-1 .card-icon.red {
  background-color: #fbe4e4;
}

.cards-1 .card-icon.red .fas,
.cards-1 .card-icon.red .far {
  color: #ef473d;
}

.cards-1 .card-icon.green {
  background-color: #e0f4ea;
}

.cards-1 .card-icon.green .fas,
.cards-1 .card-icon.green .far {
  color: #16c66d;
}


@media screen and (max-width: 500px) {
  .cards-1 {
    padding-top: 5rem;

    & .card-main {
      gap: 5px;
      flex-direction: column;
    }

    & .card {
      margin-bottom: 1rem;
    }
  }
}
</style>
