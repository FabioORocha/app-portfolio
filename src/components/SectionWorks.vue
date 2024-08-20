<template>
  <div>
    <nav class="container">
      <div class="work">
        <h2 class="title">Destaques Vnda</h2>
        <div class="wrapper">
          <div class="item" v-for="img in images" :key="img.id">
            <a :href="img.link" class="inner-btn" target="_blank" rel="noopener noreferrer">
              <img :src="img.srcImage" :alt="img.alt" class="image"/>
            </a>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        images: [
          { id: 0,  srcImage: require('../assets/01-afluente.png'), alt: 'afluente', link:'www.afluente.art' },
          { id: 1,  srcImage: require('../assets/02-casakaua.png'), alt: 'casakaua', link:'www.casakaua.com.br' },
          { id: 2,  srcImage: require('../assets/03-elisaatheniense.png'), alt: 'elisaatheniense', link:'www.elisaatheniense.com.br' },
          { id: 3,  srcImage: require('../assets/04-gabardinacouro.png'), alt: 'gabardinacouro', link:'www.gabardinacouro.com' },
          { id: 4,  srcImage: require('../assets/05-guriainspira.png'), alt: 'guriainspira', link:'www.guriainspira.com.br' },
          { id: 5,  srcImage: require('../assets/06-dbz.png'), alt: 'dbz', link:'www.dbzjeans.com.br' },
          { id: 6,  srcImage: require('../assets/07-oticas.png'), alt: 'oticas', link:'www.oticasbrasil.com.br' },
          { id: 7,  srcImage: require('../assets/08-rosanajoias.png'), alt: 'rosanajoias', link:'www.rosanajoias.com.br' },
          { id: 8,  srcImage: require('../assets/09-adoroit.png'), alt: 'adoroit', link:'www.adoroit.com.br' },
          { id: 9,  srcImage: require('../assets/10-vanquisher.png'), alt: 'vanquisher', link:'www.vanquisher.com.br' },
        ]
      }
    }
  }
</script>

<style scoped>
  .container{
    max-width: 1280px;
    margin: auto;
    display: flex;
    align-items: center;
    padding-left: 5%;
    padding-right: 5%;
  }

  .work {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border: 1px solid gray;
    padding: 4rem 1rem;
    border-radius: 33px;
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
    width: 100%;
  }

  .title{
    padding: 0 5%;
    margin-top: 2rem;
    margin-bottom: 4rem;
  }

  .wrapper{
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    gap: 1rem;
    width: 100%;
  }

  .item{
    overflow: hidden;
    padding: 0;
    width: 100%;
    height: 100%;
  }

  .image{
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: opacity 0.3s ease, transform 0.3s ease;

    &:hover{
      opacity: .8;
      transform: scale(1.05);
      transition: ease .3;
    }
  }
  
  .subtitle{
    font-size: 1rem;
    padding-top: .5rem;
  }

  @media (max-width: 680px) {
    .container{
      margin-top: 4rem;
    }

    .card{
      width: 100%;
    }
    
    .item{
      margin-right: 0 !important;
    }

    .wrapper{
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1.5rem;
    }
  }


</style>