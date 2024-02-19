<script>
	import Contactanos from './Contactanos.svelte';
import Banners from "../../Banners/Banners.svelte";
import BannerTratamiento from "../../Banners/BannerTratamiento.svelte";
import BannerEquiDoc from "../../Banners/BannerEquiDoc.svelte";
// mapa
import Mapa from "../../Componentes/Mapa.svelte";

let videoId = "ORQwM8ZhGGQ?si=BygP4oAo27wdtHNN";
// BRAKETS
// https://youtu.be/ORQwM8ZhGGQ?si=BygP4oAo27wdtHNN
// IMPLANTE DENTAL
// https://youtu.be/y0mxd29n-B0?si=cCm46zA7RDW1RGs_
// PRÓTESIS
// https://youtu.be/h3gjk8d3Eik?si=OiKUZ_Y4p5ZxObiq
// EXODONCIA COMPLEJA
// https://youtu.be/f436r8y0W6Q?si=IGw9VQqUuYqsOzu8
const videos = [
    { id: "ORQwM8ZhGGQ?si=BygP4oAo27wdtHNN", image: "ortodoncias-dentales-v2.jpg", title: " BRACKETS" },
    { id: "y0mxd29n-B0?si=cCm46zA7RDW1RGs_", image: "implantologia-dental-v2.jpg", title: "IMPLANTE DENTAL" },
    { id: "h3gjk8d3Eik?si=OiKUZ_Y4p5ZxObiq", image: "protesis-dental-2.jpg", title: "PRÓTESIS" },
    { id: "f436r8y0W6Q?si=IGw9VQqUuYqsOzu8", image: "Cirugia-Maxilofacial.jpg", title: "Cirugía Maxilofacial" }
  ];
  const cambiarVideo = (nuevoVideoId) => {
    videoId = nuevoVideoId;
  }
</script>

<main class="container">
  <!-- BANNRS DEL PRINCIPIO DE PAGINA -->
    <Banners />
    <br>
    <button class="btn btn-agenda">
      <i class="bi bi-whatsapp"></i>
      Agenda tu Primera Cita Gratis
    </button>
    <div class="tratamientos">
      <h1>TRATAMIENTOS</h1>
      <h2>Conoce nuestros Tratamietos</h2>
      <p>Todos nuestros tratamientos y servicios se brindan en cómodas instalaciones con los más altos estándares de calidad.</p>
    </div>

    <!-- BANNERS DE LOS TRATAMIENTOS -->
    <div class="banner-tratamiento">
      <BannerTratamiento />
    </div>

    <!-- DEV PARA MOSTRAR VIDEOS -->
    <div class="reproductor">
      <!-- svelte-ignore a11y-missing-attribute -->
      <iframe
          width="560"
          height="315"
          src={`https://www.youtube.com/embed/${videoId}?autoplay=1`}
          frameborder="0"
          allow="autoplay; fullscreen"
          allowfullscreen
    ></iframe>
  </div>


<!-- DIV PARA LOS BOTONES DE SELECCION DE VIDEOS -->
<div class="botones-videos">
  <h2>VIDEOS DE TRATAMIENTOS</h2>
  <div class="buttons-container">
      {#each videos as video}
      <div class="button-wrapper">
        <button on:click={() => cambiarVideo(video.id)}>
          <img src={`banner/${video.image}`} alt={video.title}>
        </button>
        <p>{video.title}</p>
      </div>
    {/each}
  </div>
</div>
    <!-- PARTE DE LAS PROMOCIONES -->
    <div class="promocion">
      <div class="contenido">
        <p class="titulo-promo" style="font-size: 30px;">PROMOCIONES ESPECIALES.</p>
        <p style="font-size: 20px;">Pregunta por las promociones especiales que tenemos para los jóvenes de entre 16 a 28 años.</p>
      </div>
      <div class="btn-promocion">
        <button class="btn btn-pro ">
          <i class="bi bi-whatsapp"></i>
          Agenda tu Primera Cita Gratis
        </button>
      </div>
    </div>

    <!-- BIENVENIDA -->
    <div class="bienvenida">
      <div class="img-bienvenida">
        <img src="img/sonrisa.png" alt="">
      </div>
      <div class="bienvenida-contenido">
        <h2>Bienvenidos a La Clínica Dental</h2>
        <strong> Expertos en tratamientos Dentales en México</strong>
        <p>Recibe el tratamiento dental que necesitas.</p>
        <p>Somos un clínica dental especializada con altos estándares de calidad para brindarte servicio de primer nivel.</p>
        <div class="iconos">
          <div class="icono">
            <img src="img/odontologia-general.png" alt="">
            <p>Odontología de Avanzada</p>
          </div>
          <div class="icono">
            <img src="img/equipos.png" alt="">
            <p>Equipos de Alta Tecnología</p>
          </div>
          <div class="icono">
            <img src="img/oficinas.png" alt="">
            <p>Oficinas Confortables</p>
          </div>
          <div class="icono">
            <img src="img/amigable.png" alt="">
            <p>Equipo Amigable</p>
          </div>
        </div>
      </div>
    </div>

    <!--  DIV DE SEPARACION CON RENUEVA TU SONRISA -->
    <div class="renueva">
      <h2 class="ren-son">¡RENUEVA TU SONRISA HOY!</h2>
      <button class="btn btn-pro ">
        <i class="bi bi-whatsapp"></i>
        Agenda tu Primera Cita Gratis
      </button>
    </div>

    <!-- DIV DE RESULTADOS INCREIBLES -->
    <div class="resultados">

    </div>
    
    <!-- DIV DE INSTALACIONES -->
    <div class="instalaciones">
      <div class="contenido-insta">
        <h2>Conoce Nuestras Instalaciones</h2>
        <p>Ofecemos servicios dentales en instalaciones de primer nivel.</p>
        <p>En nuestra clínica dental, estamos comprometidos a brindarte una sonrisa saludable y radiante. Con un ambiente cálido y acogedor, te ofrecemos un cuidado dental excepcional para que te sientas bienvenido y cómodo durante tu visita.</p>

        <div class="boton-insta">
          <button class="btn btn-insta ">
            <i class="bi bi-whatsapp"></i>
            Agenda tu Primera Cita Gratis
          </button>
        </div>
      </div>
      <div class="img-insta">
        <img src="img/instalaciones.png" alt="">
      </div>
    </div>

    <!-- <div class="nuestroEquipo">
      <h1>NUESTRO EQUIPO</h1>
      <h2>Dentistas de Primeras</h2>
      <p>En <strong>La Clínica Dental</strong> disponemos de un equipo profecional de dentistas altamente calificados, comprometidos en ofrecerte un servicio de calidad con tecnología avanzada.</p>
    </div> -->

    <!-- BANNER DEL EQUIPO DE DOCTORES -->
    <!-- <div class="nuestroEquipoBanners">
      <BannerEquiDoc />
      <div>
        <h5>Nuestros doctores</h5>
      </div>
    </div> -->

    <!--  -->

    <!-- Mapa -->
    <div class="map-forms">
      <div class="forms">
        <h1>Contactanos</h1>
        <h3>Agenda tu primera cita GRATIS</h3>
        <p>Todos nuestros servicios de atención dental se brindan en cómodas instalaciones, con citas convencionales por la mañana, tarde y los sábados. Contamos con consultorios odontológicos modernos de primera calidad y un equipo altamente capacitado de dentistas y asistentes dentales.</p>
        <div class="contacto">
          <div class="inputs">
            <div class="mb-3">
              <label for="nombre" class="form-label">Nombre</label>
              <input type="text" class="form-control" id="nombre">
            </div>
            <div class="mb-3">
              <label for="telefono" class="form-label">Teléfono</label>
              <input type="tel" class="form-control" id="telefono">
            </div>
          </div>
          <div class="mb-3">
            <label for="correo" class="form-label">Correo</label>
            <input type="email" class="form-control" id="correo">
          </div>
          <div class="mb-3">
            <label for="mensaje" class="form-label">Mensaje</label>
            <textarea class="form-control" id="mensaje" rows="3"></textarea>
          </div>
        </div>
        <button class="btn btn-success btn-enviar">Enviar</button>
      </div>
      <div id="map">
        <Mapa />
      </div>
    </div>
    

    <!-- INFORMACION DE CONTACTO -->
    <div class="contactos">
      <!-- <img src="img/informacion.png" alt=""> -->
      <div class="row">
        <div class="col-12 col-sm-3 logo-llamada">
          <img src="logos/logo-llamada.png" alt="">
          <div class="contenido-contactos">
            <p>Llámanos</p>
            <p>5589003683</p>
          </div>
        </div>
        <div class="col-12 col-sm-3 logo-llamada">
          <img src="logos/logo-ubicacion.png" alt="">
          <div class="contenido-contactos">
            <p>Dónde Estamos</p>
            <p>Google Maps</p>
          </div>
        </div>
        <div class="col-12 col-sm-3 logo-llamada">
          <img src="logos/logo-horarios.png" alt="">
          <div class="contenido-contactos">
            <p>Horarios</p>
            <p class="contacto-horarios">Lun - sab: 9:00 am - 8:00 pm</p>
          </div>
        </div>
        <div class="col-12 col-sm-3 logo-llamada">
          <img src="logos/logo-escriben.png" alt="">
          <div class="contenido-contactos">
            <p>Escribenos</p>
            <p class="contacto-email">contacto@laclinicalasaguilas.dental</p>
          </div>
        </div>
      </div>
    </div>
</main>

<style>
/* COLOR QUE SE USA EN lCD color azul:#5EBCD6    color morado: #E045EB*/
  .btn-agenda{
    background-color:#5EBCD6;
    color: white;
    margin-left: 10%;
  }
  /* PARA LOS ESTILOS DEL TRATAMIENTOS */
  .tratamientos{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    gap: 3px;
  }
  .tratamientos h1 {
    font-size: 40px;
  }
  .tratamientos h2 {
    text-align: center;
    width: 70%;
    border-bottom: 2px solid #E045EB;
  }
  .tratamientos p {
    font-size: 20px;
  }
  @media screen and (max-width: 768px) {
    .tratamientos h1 {
        font-size: 32px; 
    }

    .tratamientos h2 {
        width: 90%; 
    }

    .tratamientos p {
        font-size: 16px; 
    }
}
  /* @media screen and (min-width: 960px) {
     .tratamientos {
       flex-direction: row;
       justify-content: space-around;
     }
     .tratamientos h1, .tratamientos h2 {
       flex: 1;
     }
   } */

   .banner-tratamiento{
    margin-bottom: 60px;
   }
  /* Estilos de el div de promocion */
  .promocion{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    padding: 10px;
    box-shadow: 0px 5px 15px rgba(0,0,0,.1);
    text-shadow: 1px 1px 2px #fcfcfc;
    border-radius: 10px;
    background: linear-gradient(to right, #5EBCD6, white); 
    margin-bottom: 100px;
  }
  .titulo-promo::after {
  content: "";
  display: block;
  width: 60%; 
  border-bottom: 2px solid #E045EB;
}
   /*  Estilos para el boton de la cita gratuita */
  .btn-pro{
    border: 1px solid ;
    margin-left: 10px;
    background-color: #5EBCD6;
    color: white;
  }
  .btn-pro:hover{
    color: white !important;
    background-color: rgb(46, 188, 158);
    border: 1px solid #5EBCD6;
  }
  /* Estilos responsivos */
@media screen and (max-width: 768px) {
    .promocion {
        padding: 5px; 
    }

    .btn-pro {
        margin-left: 5px; 
    }
}

/* ESTILOS DE LAS PROMOCIONES */
.promocion {
  display: grid;
  grid-template-columns: auto auto; 
  gap: 20px; 
}

.btn-promocion {
  display: flex;
  align-items: center; 
}
/* Estilos responsivos */
@media screen and (max-width: 768px) {
    .promocion {
        grid-template-columns: 1fr; 
    }

    .btn-promocion {
        justify-content: center; 
        margin-top: 10px; 
    }
}

/* ESTILOS DE LA BIENVENIDA */
.bienvenida {
  display: flex;
  margin-bottom: 50px;
}
.bienvenida h2::after{
  content: "";
  display: block;
  width: 60%;
  height: 4px;
  border-bottom: #E045EB solid;
}

.img-bienvenida {
  flex: 0 0 auto;
  margin-right: 20px;
}

.bienvenida-contenido {
  flex: 1;
}

.iconos {
  display: flex;
  flex-wrap: wrap;
}

.icono {
  flex: 1 1 50%; 
  margin-bottom: 20px;
  display: flex;
  align-items: center;
  border-radius: 15px;
}

.icono img {
  border-radius: 50%;
  width: 100px; 
  height: 100px; 
  object-fit: cover; 
}
/* Estilos responsivos bienvenida */
@media screen and (max-width: 767px) { 
    .bienvenida {
        flex-direction: column; 
        align-items: center; 
    }

    .img-bienvenida {
        margin-right: 0; 
        margin-bottom: 20px;
    }

    .iconos {
        order: -1; 
        margin-top: 20px;
    }
}


/* ESTILOS DE RENOVACION */
.renueva{
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  padding: 10px;
  background: linear-gradient(to left, #5EBCD6, white); 
  margin-bottom: 60px;
}

.ren-son{
  margin-right: 200px;
}
/* Estilos responsivos */
@media screen and (max-width: 768px) {
    .ren-son {
        margin-right: 0; 
        margin-bottom: 20px;
    }
}

/* ESTILO DE LA INSTALACION */
.instalaciones {
  display: flex;
  justify-content: space-between; 
  align-items: center; 
  margin-bottom: 80px;
  margin-left: 30px; 
}
.instalaciones h2::after {
  content: "";
  display: block;
  width: 50%; 
  border-bottom: 2px solid #E045EB;
}


.contenido-insta {
  flex: 1; 
  margin-right: 20px; 
  display: flex;
  flex-direction: column; 
  justify-content: center; 
  margin-left: 10px;
}

.img-insta img {
  width: 100%; 
  max-width: 400px; 
  margin-right: 20px;
}

.btn-insta{
    border: 1px solid black;
    margin-left: 10px;
    background-color:#5EBCD6;
    color: white;
  }
  .btn-insta:hover{
    color: white !important;
    background-color: rgb(46, 188, 158);
    border: 1px solid #5EBCD6;
  }
  /* Estilos responsivos */
  @media screen and (max-width: 767px) {
    .instalaciones {
        flex-direction: column-reverse; 
        align-items: center; 
        margin-left: 0; 
    }

    .contenido-insta {
        text-align: center; 
        margin-right: 0; 
    }

    .img-insta img {
        margin-bottom: 20px; 
    }

    .boton-insta {
        margin-top: 20px;
    }
}

/* ESTILOS PARA EL FORMS Y EL MAPA  */
.map-forms {
  display: flex;
  margin-left: 35px;
}
.map-forms h1{
  margin-left: 0px;
  border-bottom: #E045EB 2px solid;
  width: 360px;
}
.map-forms h3{
  margin-left: 0px;
}

.forms {
  flex: 1; 
}

#map {
  flex: 1; 
}
.forms {
  flex: 1;
  padding-right: 20px; 
}

.contacto {
  background-color: #f8f9fa; 
  padding: 20px;
  border-radius: 10px; 
}

.form-label {
  font-weight: bold; 
}

.form-control {
  width: 100%; 
  margin-bottom: 10px; 
}

textarea.form-control {
  resize: vertical; 
}

.inputs {
  display: flex;
  justify-content: space-between;
}
.btn-enviar{
  margin-top: 1%;
  margin-left: 35%;
  width: 30%;
}

/* mapa */
#map { height: 560px; }

@media screen and (max-width: 767px) {
  .map-forms {
    flex-direction: column;
    margin-left: 0;
  }
  .map-forms h1 {
    margin-left: 0;
    width: auto;
    text-align: center;
  }
  .map-forms h3 {
    margin-left: 0;
    text-align: center;
  }
  .forms {
    padding-right: 0;
  }
  .contacto {
    border-radius: 0; 
  }
  .form-control {
    width: calc(100% - 20px); 
  }
  .inputs {
    flex-direction: column; 
  }
  .img-insta img {
    margin-right: 0; 
  }
}

/* ESTILOS DE LOS ICONOS DE CONTACTO */
.contactos{
  margin-top: 60px;
  margin-bottom: 30px;
}

.logo-llamada{
  display: grid;
  grid-template-columns: 1fr 1fr;
}
@media screen and (max-width: 767px){
  .logo-llamada{
    display: flex;
    flex-direction: column; 
    justify-content: center; 
    align-items: center; 
    text-align: center;
  }
}

/* ESTILOS PARA EL AJUSTE DEL VIDEO */
/* .reproductor {
        position: absolute; 
        top: 100%; 
        left: 50%; 
        transform: translate(-50%, -50%); 
       
    } */
.reproductor {
  display: flex;
  justify-content: center;
  margin-bottom: 20px;
}
.reproductor iframe{
  -webkit-box-shadow: 13px 16px 5px 0px rgba(0,0,0,0.45);
    -moz-box-shadow: 13px 16px 5px 0px rgba(0,0,0,0.45);
    box-shadow: 13px 16px 5px 0px rgba(0,0,0,0.45);
}

/* ESTILOS PARA LOS BOTONES PARA CAMBIAR LOS VIDEOS */
.botones-videos {
    /* background-color: rgba(224, 69, 235, 0.7); */
    background-color: #b969de89;
    padding: 20px; 
    margin-bottom: 50px;
    margin-top: 10px;
}

.botones-videos h2 {
    margin-bottom: 10px;
    text-align: center;
    color: white;
}

.buttons-container {
    display: flex;
    justify-content: center;
}

.button-wrapper {
    text-align: center;
    margin: 0 10px; 
}

.button-wrapper button {
    border: none;
    background: none;
    cursor: pointer;
}


.button-wrapper button:hover 
{animation:rotate-scale-up 0.4s linear both} 
@keyframes rotate-scale-up{
  0%{transform:scale(1) rotateZ(0)}
  50%{transform:scale(2) rotateZ(180deg)}
  100%{transform:scale(1) rotateZ(360deg)}
}
.button-wrapper img {
    width: 100px; 
    height: 100px; 
    border-radius: 50%; 
    object-fit: cover; 
  }
.button-wrapper p{
  color: white;
}

/* Estilos para dispositivos móviles botones-videos*/
@media screen and (max-width: 800px) {
  .botones-videos {
    padding: 10px; 
  }

  .botones-videos h2 {
    font-size: 1.2rem; 
  }

  .buttons-container {
    flex-direction: column;
  }

  .button-wrapper {
    margin: 10px 0; 
  }
}
  
</style>
 