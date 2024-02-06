<script>
import Banners from "../../Banners/Banners.svelte";
import BannerTratamiento from "../../Banners/BannerTratamiento.svelte";
import BannerEquiDoc from "../../Banners/BannerEquiDoc.svelte";
// mapa
import Mapa from "../../Componentes/Mapa.svelte";
</script>

<main>
  <!-- BANNRS DEL PRINCIPIO DE PAGINA -->
    <Banners />
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
    <BannerTratamiento />
    <!-- PARTE DE LAS PROMOCIONES -->
    <div class="promocion">
      <div class="contenido">
        <p style="font-size: 30px;">PROMOCIONES ESPECIALES.</p>
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
    <div id="map">
      <Mapa />
    </div>
</main>

<style>
/* COLOR QUE SE USA EN lCD #5EBCD6 */
  .btn-agenda{
    background-color:#5EBCD6;
    color: white;
    margin-right: 10px;
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
    border-bottom: 2px solid #5EBCD6;
  }
  .tratamientos p {
    font-size: 20px;
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
  }

   /*  Estilos para el boton de la cita gratuita */
  .btn-pro{
    border: 1px solid black;
    margin-left: 10px;
  }
  .btn-pro:hover{
    color: white !important;
    background-color: rgb(46, 188, 158);
  }

/* ESTILOS DE LAS PROMOCIONES */
.promocion {
  display: grid;
  grid-template-columns: auto auto; /* Columna 1 para el contenido, columna 2 para el botón */
  gap: 20px; /* Espacio entre las columnas */
}

.btn-promocion {
  display: flex;
  align-items: center; /* Centra el botón verticalmente */
  /* border: 0; */
}

/* ESTILOS DE LA BIENVENIDA */
.bienvenida {
  display: flex;
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
  flex: 1 1 50%; /* Dos iconos por fila */
  margin-bottom: 20px;
  display: flex;
  align-items: center;
  border-radius: 15px;
}

.icono img {
  border-radius: 50%; /* Hace que la imagen tenga bordes redondeados */
  width: 100px; /* Ajusta el ancho de la imagen según sea necesario */
  height: 100px; /* Ajusta la altura de la imagen según sea necesario */
  object-fit: cover; /* Ajusta el tamaño de la imagen para que cubra completamente el contenedor */
}


  /* Estilo para nuestro equipo */
  /* .promocion{
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    gap: 3px;
    height: 30vh;
    
    flex-wrap: wrap;
  } */
/* 
  .nuestroEquipo h1{
    font-size: 40px;
  }
  .nuestroEquipo h2{
    text-align: center;
    width: 70%;
    border-bottom: 2px solid #5EBCD6;
  }
  .nuestroEquipo p {
    font-size: 20px;
  }
  
  .nuestroEquipoBanners {
  display: grid;
  grid-template-columns: 1fr 2fr; 
} */

/* mapa */
#map { height: 280px; }
</style>
 