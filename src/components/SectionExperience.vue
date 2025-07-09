<template>
  <div>
    <div class="container">
      <div class="wrapper">
        <div class="card">

          <div class="vnda">
            <h2 class="title">Experiência profissional</h2>
            <div class="innerImage">
              <a href="https://www.vnda.com.br/" class="inner-btn" target="_blank" rel="noopener noreferrer">
                <img alt="Image vnda" src="../assets/vnda.png" class="image">
              </a>
            </div>
            <div class="innerText">
              <p class="textTitle">Vnda Ecommerce - 2 anos</p>
              <ul class="description">
                <li>Criei interfaces para e-commerces na Olist Vnda usando HTML, SCSS, JavaScript e LIQUID, a partir de layouts no Figma</li>
                <li>Corrigi bugs críticos que afetavam a usabilidade em dispositivos móveis.</li>
                <li>Implementei ajustes que reduziram o tempo de carregamento das lojas de forma significativa e aumentaram a nota no PageSpeed.</li>
              </ul>
            </div>
            <div class="wrapperItens">
              <div class="item" v-for="img in imagesVnda" :key="img.id">
                <img :src="img.srcImage" :alt="img.alt" class="itemImage"/>
              </div>
            </div>
          </div>

          <div class="oasis">
            <div class="innerImage">
              <a href="https://www.agenciaoasis.com.br/" class="inner-btn" target="_blank" rel="noopener noreferrer">
                <img alt="Image oasis" src="../assets/oasis.png" class="image">
              </a>
            </div>
            <div class="innerText">
              <p class="textTitle">Grupo Oásis - 5 meses</p>
              <ul class="description">
                <li>Desenvolvi interfaces completas para e-commerces na plataforma Wake Commerce</li>
                <li>Entreguei um projeto em Nuvemshop dentro do prazo, mesmo sem ter trabalhado com a plataforma antes. Fui aprendendo enquanto desenvolvia.</li>
                <li>Corrigi bugs apontados pelo time de QA e também em projetos de colegas, ajudando a manter a estabilidade das entregas</li>
                <li>Trabalhei com HTML, CSS, scss, JavaScript, Twig, Scriban, Tailwind, React e Next.js.</li>
                <li>Participei da documentação das lojas para facilitar futuras manutenções</li>
              </ul>
            </div>
            <div class="wrapperItens">
              <div class="item" v-for="img in imagesOasis" :key="img.id">
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
      imagesVnda: [
        { id: 0,  srcImage: require('../assets/html.png'), alt: 'html' },
        { id: 1,  srcImage: require('../assets/css.png'), alt: 'css' },
        { id: 2,  srcImage: require('../assets/javascript.png'), alt: 'javascript' },
        { id: 3,  srcImage: require('../assets/liquid.png'), alt: 'liquid' },
        { id: 4,  srcImage: require('../assets/sass.png'), alt: 'sass' },
        { id: 5, srcImage: require('../assets/gitlab.png'), alt: 'gitlab' },
        { id: 6, srcImage: require('../assets/figma.png'), alt: 'figma' }
      ],
      imagesOasis: [
        { id: 0,  srcImage: require('../assets/html.png'), alt: 'html' },
        { id: 1,  srcImage: require('../assets/css.png'), alt: 'css' },
        { id: 3,  srcImage: require('../assets/javascript.png'), alt: 'javascript' },
        { id: 4,  srcImage: require('../assets/twig.png'), alt: 'twig' },
        { id: 5,  srcImage: require('../assets/react.png'), alt: 'react' },
        { id: 6,  srcImage: require('../assets/next.png'), alt: 'next' },
        { id: 7,  srcImage: require('../assets/sass.png'), alt: 'sass' },
        { id: 8,  srcImage: require('../assets/tailwind.png'), alt: 'tailwind' },
        { id: 9, srcImage: require('../assets/gitlab.png'), alt: 'gitlab' },
        { id: 10, srcImage: require('../assets/figma.png'), alt: 'figma' }
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