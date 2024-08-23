<template>
  <div>
    <div class="container">
      <div class="wrapper">
        <div class="card">
          <h2 class="title">Experiência profissional</h2>
          <div class="innerImage">
            <a href="https://www.vnda.com.br/" class="inner-btn" target="_blank" rel="noopener noreferrer">
              <img alt="Image vnda" src="../assets/vnda.png" class="image">
            </a>
          </div>
          <div class="innerText">
            <p class="textTitle">Vnda Ecommerce - 2 anos</p>
            <p class="description">Desenvolvimento front-end de interfaces para e-commerces a partir de wireframes, garantindo a fidelidade visual e funcional do projeto. Realização de revisões e correções de bugs para aprimorar a experiência do usuário.</p>
          </div>
          <div class="wrapperItens">
            <div class="item" v-for="img in images" :key="img.id">
              <img :src="img.srcImage" :alt="img.alt" class="itemImage"/>
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
      images: [
        { id: 0,  srcImage: require('../assets/html.png'), alt: 'html' },
        { id: 1,  srcImage: require('../assets/css.png'), alt: 'css' },
        { id: 2,  srcImage: require('../assets/javascript.png'), alt: 'javascript' },
        { id: 3,  srcImage: require('../assets/liquid.png'), alt: 'liquid' },
        { id: 4,  srcImage: require('../assets/sass.png'), alt: 'sass' },
        { id: 5, srcImage: require('../assets/gitlab.png'), alt: 'gitlab' },
        { id: 6, srcImage: require('../assets/figma.png'), alt: 'figma' }
      ]
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