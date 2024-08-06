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

          <div class="card col-lg-4 align-items-center" v-for="(item, index) in services" :key="index">
            <div :class="`card-icon ${item.iconColor}`">
              <span :class="item.iconService"></span>
            </div>
            <div class="card-body">
              <h5 class="card-title">{{ item.name }}</h5>
              <p>{{ item.content }}</p>
              <a class="read-more no-line" href="#">Ver mais <span class="fas fa-long-arrow-alt-right"></span></a>
            </div>
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
      services: [
        { name: 'Análise de produtos', iconService: 'fas fa-headphones-alt', iconColor: 'green', content: 'Vulputate nibh feugiat. Morbi pellent diam nec libero lacinia, sed ultrices velit scelerisque. Nuncplacerat justo sem' },
        { name: 'Oportunidades', iconService: 'far fa-clipboard', iconColor: 'red', content: 'Vulputate nibh feugiat. Morbi pellent diam nec libero lacinia, sed ultrices velit scelerisque. Nuncplacerat justo sem' },
        { name: 'Comunicação', iconService: 'far fa-comments', iconColor: 'blue', content: 'Vulputate nibh feugiat. Morbi pellent diam nec libero lacinia, sed ultrices velit scelerisque. Nuncplacerat justo sem' },
        { name: 'Oportunidades', iconService: 'far fa-comments', iconColor: 'green', content: 'Vulputate nibh feugiat. Morbi pellent diam nec libero lacinia, sed ultrices velit scelerisque. Nuncplacerat justo sem' },
        { name: 'Comunicação', iconService: 'fas fa-headphones-alt', iconColor: 'red', content: 'Vulputate nibh feugiat. Morbi pellent diam nec libero lacinia, sed ultrices velit scelerisque. Nuncplacerat justo sem' },
        { name: 'Análise de produtos', iconService: 'far fa-clipboard', iconColor: 'blue', content: 'Vulputate nibh feugiat. Morbi pellent diam nec libero lacinia, sed ultrices velit scelerisque. Nuncplacerat justo sem' }
      ]
    }
  }
}

</script>

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
    max-width: 400px;
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
    flex-wrap: wrap;
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

.cards-1 .card-icon.blue {
  background-color: #282f96de;
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
      align-items: center;
    }

    & .card {
      margin-bottom: 1rem;
    }
  }
}
</style>
