<template>
  <div>
    <div class="container">
      <div class="wrapper">
        <div class="card">

          <div class="foco">
            <h2 class="title">Projetos</h2>
            <div class="innerImage">
              <img alt="Image peafoco" src="../assets/peafoco.png" class="image">
            </div>
            <div class="innerText">
              <p class="textTitle">PEA FOCO - 1 anos</p>
              <ul class="description">
                <li>Desenvolvimento e proposta de projeto.</li>
                <li>Criação do wireframe utilizando o Adobe XD.</li>
                <li>Desenvolvimento de uma aplicação mobile em React Native, HTML, Expo, JavaScript e CSS.</li>
                <li>Projeto focado em atender necessidades de cadastro de pessoas para a ONG</li>
              </ul>
            </div>
            <div class="wrapperItens">
              <div class="item" v-for="img in imagesFoco" :key="img.id">
                <img :src="img.srcImage" :alt="img.alt" class="itemImage"/>
              </div>
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
      imagesFoco: [
        { id: 0,  srcImage: require('../assets/react.png'), alt: 'react' },
        { id: 1,  srcImage: require('../assets/firebase.png'), alt: 'firebase' },
        { id: 2,  srcImage: require('../assets/github.png'), alt: 'github' },
        { id: 3,  srcImage: require('../assets/adobexd.png'), alt: 'adobexd' },
      ],
    }
  }
  }
</script>

<style scoped>

  .container{
    max-width: 1280px;
    margin: 0 auto;

    padding-left: 5%;
    padding-right: 5%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-bottom: 6rem;
  }

  .title{
    padding: 0 5%;
    margin-top: 2rem;
    margin-bottom: 2rem;
  }

  .wrapper{
    width: 100%;
    display: flex;
    margin-top: 2rem;
  }

  .card{
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 1rem;

    border: 1px solid gray;
    border-radius: 33px;
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
    background-color: #343A40;

    a{
      width: 100%;
      padding-bottom: 1rem;
    }

    .oasis{
      margin-top: 2rem;
    }
  }

  .innerImage{
    width: 100%;
    height: auto;
  }

  .image{
    width: 20%;
  }

  .innerText{
    padding-bottom: 1rem;
    display: flex;
    align-items: center;
    flex-direction: column;

    ul li{
      margin-top: 12px;
    }
  }

  .textTitle{
    font-weight: 600;
  }

  .description{
    margin: 0 auto;
    max-width: 80%;
  }

  .technology{
    width: 100%;
  }

  .wrapperItens{
    display: flex;
    justify-content: center;
    gap: 1rem;
    padding: 1rem 0;
    width: 100%;
    flex-wrap: wrap;
  }

  .item{
    display: flex;
    justify-content: center;
    box-sizing: border-box;
    width: 2rem;
  }

  .itemImage{
    width: 100%;
    height: auto;
    object-fit: contain;
  }

</style>