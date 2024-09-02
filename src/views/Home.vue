<template>
  <section>
    <section class="hero-image" id="hero-image">
      <div class="text-container">
        <p class="text-title">
          Hola mundo<span class="cursor">|</span>
        </p>
        <p class="text-info">
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aperiam
          facere quidem reiciendis soluta rerum! Debitis amet distinctio ut
          optio, nam saepe harum consequuntur numquam voluptatum, recusandae
          libero aliquid consectetur vitae.
        </p>
        <!-- <button class="btn" @click="handleLogin">Iniciar sesión</button> -->
      </div>
      <div class="img-container">
        <img class="img" src="../assets/8225847.jpg" alt="ilustracion hermosa" />
      </div>
    </section>

    <section class="card-detail">
      <div class="card-info">
        <p class="card-title">Título de información</p>
        <ul>
          <li>contacto</li>
          <li>número telefónico</li>
          <li>correo electrónico</li>
          <li>proyectos</li>
        </ul>
      </div>
      <figure class="card-preview">
        <section class="img-container">
          <b class="text-info">Hola mundo</b>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed
            consectetur viverra diam, id consectetur lectus tempus id. Nullam
            viverra, nunc id.
          </p>
          <!-- <img class="img" src="https://via.placeholder.com/100" alt="Placeholder" /> -->
        </section>
      </figure>
    </section>

    <section class="card-section">
      <p class="section-title">Información relevante</p>
      <div class="tarjetas">
        <figure class="card">
          <p class="text-title">Hola mundo</p>
          <p class="text-info">
            Lorem ipsum dolor sit amet consectetur adipisicing elit.
            Architecto perferendis dolores nam velit ducimus dolore expedita
            assumenda voluptatibus accusamus! Nam architecto porro minima,
            suscipit ratione sequi rem possimus quas modi?
          </p>
        </figure>
        <figure class="card">
          <p class="text-title">Hola mundo</p>
          <p class="text-info">
            Lorem ipsum dolor sit amet consectetur adipisicing elit.
            Architecto perferendis dolores nam velit ducimus dolore expedita
            assumenda voluptatibus accusamus! Nam architecto porro minima,
            suscipit ratione sequi rem possimus quas modi?
          </p>
        </figure>
        <figure class="card">
          <p class="text-title">Hola mundo</p>
          <p class="text-info">
            Lorem ipsum dolor sit amet consectetur adipisicing elit.
            Architecto perferendis dolores nam velit ducimus dolore expedita
            assumenda voluptatibus accusamus! Nam architecto porro minima,
            suscipit ratione sequi rem possimus quas modi?
          </p>
        </figure>
      </div>
    </section>

    <section class="video">
      <p class="section-title">Videos informativos</p>
      <div class="tarjetas">
        <figure class="card">Hola mundo</figure>
        <figure class="card">Hola mundo</figure>
        <figure class="card">Hola mundo</figure>
      </div>
    </section>

    <section class="banner-final">
      <p class="section-title">Llamado a la acción final</p>
      <div class="cards">
        <div class="card">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Architecto
          perferendis dolores nam velit ducimus dolore expedita assumenda
          voluptatibus accusamus! Nam architecto porro minima,
        </div>
        <div class="card">
          <button @click="handleReview">Dejar una pequeña reseña</button>
        </div>
      </div>
    </section>
  </section>
</template>


<script>
export default {
  name: 'HomeView',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
:root {
  /* color: #334256; */
  --text-title: #334256;
  --text-color: #656b73;

}

@import url(https://fonts.googleapis.com/css2?family=Do+Hyeon&display=swap);

.hero-image {
  height: 100vh;
  padding: 50px;

  display: flex;
  align-items: center;
  animation: blur-in 2s ease-in-out;

  /* view-timeline-name: --reveal;
  animation-fill-mode: both;
  animation-timeline: --reveal; */
  animation-name: show-hero;

  .text-container {
    padding: 40px;
    position: relative;
    width: 100%;
    text-align: left;
    font-size: larger;

    .text-title {
      color: #41464b;

      font-weight: 999;
      /* font-family: Verdana, Geneva, Tahoma, sans-serif; */
      font-size: 54px;
      animation: text-shadow 2s ease-in-out;


      /* 
      view-timeline-name: --reveal;
      animation-fill-mode: both;
      animation-timeline: --reveal; */

      animation-name: text-shadow;

      .cursor {
        visibility: hidden;
        animation: cursor 1s step-start infinite;
      }
    }

    .text-info {
      color: #656b73;
    }

    .btn {
      background: #71a3c1;
      color: #bbd6e5;
      padding: 2% 5%;
    }
  }

  .img-container {
    /* position: relative; */
    /* display: inline-block; */
    overflow: hidden;
    /* Oculta cualquier desbordamiento */
    border-radius: 15px;
    /* Redondea las esquinas del contenedor */
  }

  .img {
    /* display: block; */
    width: 70%;
    /* Ajusta el tamaño de la imagen al contenedor */
    height: auto;
    /* Mantiene la relación de aspecto */
    border-radius: 15px;
    /* Redondea las esquinas de la imagen */
    mask-image: radial-gradient(circle, rgb(0, 0, 0) 50%, rgb(255, 255, 255) 70%);
    /* Desenfoque en las orillas */
    -webkit-mask-image: radial-gradient(circle, rgb(0, 0, 0) 50%, rgb(255, 255, 255) 70%);
    /* Compatibilidad con WebKit */
  }
}

.video {
  background: #ffffff;
}

.card-section,
.video {
  /* justify-content: center; */
  padding: 20px;
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;



  width: 100%;
  margin-inline: 0vw;
  padding-inline: 5vw;

  .section-title {
    text-transform: capitalize;
    /* font-size: var(--fontSize-24); */
    line-break: anywhere;
    padding: 10px 10vw;
    font-weight: bold;
    font-family: var(--root-font), 'Manrope', sans-serif;
    color: #334256;
    font-size: 24px;
    text-align: start;
  }

  .tarjetas {
    gap: 20px;
    display: flex;
    flex-direction: row;

    /* border: dashed #ff3434; */
    .card {



      p {
        line-height: 20px;
        font-size: var(--fontSize-14);
        text-align: left;
        height: 78px;
        overflow: hidden;
        text-overflow: ellipsis;
        -webkit-line-clamp: 4;
        display: -webkit-box;
        -moz-box-orient: vertical;
      }

      /* height: 200px; */
      /* border-radius: 15px; */
      /* box-shadow: 0 0 4px 2px #cae3e895; */
      /* background: #ffffff; */
      /* color: #656b73; */
      max-width: 280px;
      height: 318px;
      color: black;
      cursor: pointer;
      border-radius: 20px;
      background-color: rgb(255, 255, 255);

      /* border: 1px solid rgb(210, 215, 217); */
      box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;

      view-timeline-name: --reveal;
      animation-fill-mode: both;
      animation: show linear;
      animation-timeline: view();
      animation-range: entry 0% cover 40%;
      /* height: 150px; */
      /* width: 25%; */
      padding: 20px;
      /* border: dashed; */
      flex: 1;
      /* space-around */

    }

    .card:hover {
      transform: scale(1.04);
      transition: transform 1s;
      background-color: #00ff73;
      border: 1px solid rgb(210, 215, 217);
      /* box-shadow: 0 0 6px 2px #b9c9cfd4; */
    }

  }
}

.banner-final {
  /* border: dashed #B3BBC1; */
  margin: 0 0 20px 0;
  padding: 20px;
  background-color: #fff0e6;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 2;

  .section-title {
    /* border: dashed #49ac46; */
    color: #2c3034;
    font-stretch: expanded;
    text-align: center;
    font: 2em sans-serif;
    font-weight: bold;

  }

  .cards {
    display: flex;
    justify-content: center;
    align-items: center;
    justify-items: center;
    flex-direction: column;
    gap: 20px;

    .card {
      color: #4681ac;
      font-family: 'Do Hyeon', sans-serif;
      text-align: -webkit-center;
      margin: 20px;

      button {
        border: #4681ac solid;
        padding: 10px;
        color: #ffffff;
        background-color: #4681ac;
      }

    }

    /* border: dashed #b59701; */
  }

}



/* animations */

@keyframes dropAnimation {
  0% {
    transform: translateY(-100%);
    opacity: 0;
  }

  50% {
    opacity: 1;
  }

  100% {
    transform: translateY(100vh);
    opacity: 0;
  }
}

@keyframes borderBlink {

  0%,
  100% {
    box-shadow: 0 0 0 2px rgb(255, 204, 0), 0 0 0 10px rgb(247, 242, 188);
  }

  50% {
    box-shadow: 0 0 0 1px rgba(248, 231, 28, 0), 0 0 0 5px rgba(248, 231, 28, 0);
  }
}

/* visibility: visible; */

@keyframes text-shadow {
  0% {
    opacity: 0;
    font-size: 30px;
    text-shadow: 15px 15px #e0ace4;
  }

  50% {
    opacity: 1;
    text-shadow: -15px -15px #9bcae3;

  }

  80% {
    opacity: 1;
    text-shadow: -55px 25px #e1d1d1;
  }


  100% {
    opacity: 1;
    text-shadow: -50px 55px #f6f6f6;
  }
}

@keyframes cursor {
  50% {
    visibility: visible;
    /* color: darkblue; */
  }
}

@keyframes blur-in {
  from {
    opacity: 0;
    filter: blur(4px);
  }

  to {
    opacity: 1;
    filter: blur(0);
  }
}

@keyframes show {
  from {
    opacity: 0;
    scale: 0.20;
    filter: blur(2px);

    /* transform: scale(1.40); */

  }

  to {
    opacity: 1;
    scale: 1;

    filter: blur(0);
  }
}

@keyframes show-hero {


  from {
    opacity: 0;
    /* transform: scale(1.40); */
    filter: blur(2px);
  }

  to {
    opacity: 1;
    filter: blur(0);
  }
}

.card-detail {

  padding: 20px;
  display: flex;
  flex-direction: row;
  /* color: #93bdd4; */
  background-color: #d4ffea;
  box-shadow: 0 0 0 1px rgba(248, 231, 28, 0), 0 0 0 5px rgba(248, 231, 28, 0);
  text-align: start;

  .card-info {
    flex: 1;
    width: 10%;
    margin: 0 0 0 5%;

    /* border: dashed; */
    ul {
      list-style-type: none;
      /* border dashed; */
      padding: 0;
      margin: 0;

      li {
        line-height: 20px;
        text-align: left;
        /* overflow: hidden; */
        /* text-overflow: ellipsis; */
        margin-bottom: 10px;
      }
    }

    .card-title {
      font-size: 24px;
      font-weight: bold;
      /* color: #4681ac; */

    }
  }

  .card-preview {
    background: #ffd8fc;
    flex: 2;
    padding: 20px;
    margin: 20px;
    display: flex;

    flex-direction: column;

    width: auto;

    .img-container {
      display: flex;
      flex-direction: row;
      justify-content: space-between;

      .text-info {
        font-size: xxx-large;
        color: #2d9f8c;
      }

      p {
        color: #334256;
        margin: 0 30% 0 0;
      }

      .img {
        display: flex;
        justify-self: start;
        align-items: end;
        /* width: 10%; */
        border-radius: 50%;
        width: 50px;
        height: 50px;

      }
    }

    .footerFin {}

  }
}
</style>
