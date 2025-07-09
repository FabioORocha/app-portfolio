<template>
  <div>
    <section class="container">
      <div class="card">
        <h2 class="title">Conhecimentos</h2>
        <div class="wrapper">
          <div class="item" v-for="img in images" :key="img.id">
            <img :src="img.srcImage" :alt="img.alt" class="image"/>
            <p class="txt-subtitle">{{ img.alt }}</p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>


<script>
export default {
  data() {
    return {
      images: [
        { id: 0,  srcImage: require('../assets/html.png'), alt: 'html' },
        { id: 1,  srcImage: require('../assets/css.png'), alt: 'css' },
        { id: 1,  srcImage: require('../assets/tailwind.png'), alt: 'tailwind' },
        { id: 7,  srcImage: require('../assets/sass.png'), alt: 'sass' },
        { id: 2,  srcImage: require('../assets/javascript.png'), alt: 'javascript' },
        { id: 3,  srcImage: require('../assets/liquid.png'), alt: 'liquid' },
        { id: 3,  srcImage: require('../assets/twig.png'), alt: 'twig' },
        { id: 4,  srcImage: require('../assets/react.png'), alt: 'react' },
        { id: 5,  srcImage: require('../assets/next.png'), alt: 'next' },
        { id: 6,  srcImage: require('../assets/vue.png'), alt: 'vue' },
        { id: 8,  srcImage: require('../assets/git.png'), alt: 'git' },
        { id: 9,  srcImage: require('../assets/github.png'), alt: 'github' },
        { id: 10, srcImage: require('../assets/gitlab.png'), alt: 'gitlab' },
        { id: 11, srcImage: require('../assets/figma.png'), alt: 'figma' },
        { id: 12, srcImage: require('../assets/firebase.png'), alt: 'firebase' }
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
    padding-bottom: 0;
    margin-bottom: 0;
    margin-top: 2rem;
  }

  .card {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border: 1px solid gray;
    padding: 4rem 1rem;
    border-radius: 33px;
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
    width: 100%;
    background-color: #343A40;
  }

  .title{
    padding: 0 5%;
    margin-top: 2rem;
    margin-bottom: 4rem;
  }

  .wrapper{
    display: flex;
    justify-content: center;
    align-items: center;
    gap: .2rem;
    flex-wrap: wrap;
  }

  .item{
    overflow: hidden;
    padding: .5rem;
  }

  .image{
    width: 60px;
    height: 60px;
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

  .txt-subtitle{
    font-size: 1rem;
    margin: 0;
    margin-top: 10px;
  }


  @media (max-width: 1024px) {
    .container{
      margin-top: 2rem;
    }

    .card{
      width: 100%;
    }
    
    .item{
      margin-right: 0 !important;
      margin-bottom: 1rem;
    }

    .wrapper{
      display: flex;
      flex-wrap: wrap;
    }
  }

</style>