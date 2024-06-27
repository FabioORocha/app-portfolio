<template>
  <div>
    <section class="container">
      <div class="card">
        <div class="innerimage">
          <img alt="Image profile" src="../assets/portfolio.png" class="image">
          <h2 class="name">Fábio Oliveira da Rocha</h2>
          <h2 class="role">Desenvolvedor Front-End</h2>
  
          <div class="btn">
            <a href="https://www.linkedin.com/in/fabiooliveiradarocha/" class="inner-btn" target="_blank" rel="noopener noreferrer">
              <font-awesome-icon :icon="['fab', 'linkedin']" />
              <p>LinkedIn</p>
            </a>
            <a href="https://github.com/FabioORocha" class="inner-btn" target="_blank" rel="noopener noreferrer">
              <font-awesome-icon :icon="['fab', 'github']" />
              <p>GitHub</p>
            </a>
          </div>
        </div>
        <div class="innertext">
          <h2 class="title">
            Olá, sou o <strong>Fábio</strong>!
          </h2>
          <p class="content">
            Estou buscando novos desafios e oportunidades como Desenvolvedor Front-End!
          </p>
          <p class="content">
            Tenho dois anos de experiência como desenvolvedor front-end em uma empresa focada em e-commerces, conquistei habilidades para criar interfaces dinâmicas, responsivas e alinhadas aos propósitos de diversas lojas.
          </p>
          <p class="content">
          Trabalho com foco em refletir a essência de cada marca e impulsionar o sucesso comercial online.
          </p>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
  export default {
    
  }
</script>

<style scoped>

  .container{
    max-width: 1280px;
    margin: auto auto;
    display: flex;
    align-items: center;
    padding-left: 5%;
    padding-right: 5%;
    margin-bottom: 4rem;
    min-height: calc(100vh - 50px);

    .card{
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 4rem;
      border: 1px solid gray;
      padding: 4rem 0;
      border-radius: 33px;
      box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
    
    }

    .innerimage{

      display: flex;
      flex-direction: column;
      align-items: center;

      .image{
        overflow: hidden;
        border-radius: 50%;
        width: 300px;
        height: 300px;
      }

      .name{
        margin-bottom: 0;
        font-size: 1.375rem;
        font-weight: 600;
      }

      .role{
        margin-bottom: 2rem;
        font-size: 1.125rem;
        font-weight: 400;
      }

      .btn{
        display: flex;
        gap: 1rem;

        .inner-btn{
          display: flex;
          align-items: center;
          justify-content: center;
          gap: 1rem;
          padding: 2px 1rem;
          border-radius: 1rem;
          background-color: #f1f1f1;
          color: #000000;
          text-decoration: none;
          min-width: 144px;

          &:hover{
            color: #8D8C8D;
          }
        }

        a svg{
          width: 1.5rem;
          height: 1.5rem;
        }
      }
    }

    .innertext{
      font-size: 1.125rem;
      font-weight: 600;
      max-width: 40%;

      .title{
        font-size: 3.375rem;

        strong{
          color: purple;
        }
      }

      .content{
        font-size: 1rem;
        font-weight: 500;
        line-height: 1.5rem;
      }
    }

    @media(max-width: 680px){
      flex-direction: column;
      gap: 2rem;
      margin-top: 4rem;
      margin-bottom: 4rem;

      .innerimage .image{
        margin: 0 auto;
        overflow: hidden;
        width: 50%;
        height: auto;
        aspect-ratio: 1/1;
      }

      .innertext{
        max-width: initial;
        text-align: center;
      }
    }
  }


</style>