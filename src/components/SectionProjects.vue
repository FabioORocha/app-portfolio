<template>
  <div>
    <section class="container">
      <div class="work">
        <h2 class="title">Projetos recentes</h2>
        <div class="wrapper">
          <div class="item" v-for="img in images" :key="img.id">
            <a :href="img.link" class="inner-img" target="_blank" rel="noopener noreferrer">
              <img :src="img.srcImage" :alt="img.alt" class="image"/>
            </a>
            <div class="text">
              <h4>{{ img.title }}</h4>
              <p>{{  img.description }}</p>
              <a :href="img.link" class="link" target="_blank" rel="noopener noreferrer">
                Acesse aqui
              </a>
            </div>
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
          { id: 0,  srcImage: require('../assets/01-2bstore.png'), alt: '2bstore', link:'https://marketplace-sigma-eight.vercel.app/', title:'Marketplace', description:'Desenvolvido um marketplace com homepage, pagina de produto, carrinho funcional e postado na versel utilizando framework react.js' },
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
    margin-top: 2rem;
  }

  .work {
    border: 1px solid gray;
    padding: 4rem 5%;
    border-radius: 33px;
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
    width: 100%;
    background-color: #343A40;
    margin-bottom: 4rem;
  }

  .title{
    padding: 0 5%;
    margin-top: 2rem;
    margin-bottom: 4rem;
  }

  .wrapper{
    width: 100%;
  }

  .item{
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0;
    width: 100%;
    height: 100%;

    &:nth-child(even){
      flex-direction: row-reverse;
    }

    &:not(:last-child){
      margin-bottom: 4rem;
    }
  }

  .inner-img{
    width: 100%;
  }

  .image{
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: opacity 0.3s ease;

    &:hover{
      opacity: .8;
      transition: ease .3;
    }
  }

  .text{
    padding: 0 5%;
    max-width: 60%;
  }

  .link{
    color: #fff;
  }
  
  .subtitle{
    font-size: 1rem;
    padding-top: .5rem;
  }

  @media (max-width: 680px) {

    .card{
      width: 100%;
    }
    
    .item{
      flex-direction: column;
      margin-right: 0 !important;

      &:nth-child(even){
        flex-direction: column;
      }
    }

    .text{
      max-width: 100%;
    }

    .wrapper{
      flex-direction: column;
      gap: 1.5rem;
    }
  }


</style>