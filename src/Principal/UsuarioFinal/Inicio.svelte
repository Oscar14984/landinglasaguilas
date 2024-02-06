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
    <div class="promocion">
      <p>PROGRAMA UNA CITA PARA UNA <strong>CONSULTA GRATIS.</strong></p>
      <button class="btn btn-promocion">
        <i class="bi bi-whatsapp"></i>
        Agenda tu Primera Cita Gratis
      </button>
    </div>
    <div class="nuestroEquipo">
      <h1>NUESTRO EQUIPO</h1>
      <h2>Dentistas de Primeras</h2>
      <p>En <strong>La Clínica Dental</strong> disponemos de un equipo profecional de dentistas altamente calificados, comprometidos en ofrecerte un servicio de calidad con tecnología avanzada.</p>
    </div>

    <!-- BANNER DEL EQUIPO DE DOCTORES -->
    <div class="nuestroEquipoBanners">
      <BannerEquiDoc />
      <div>
        <h5>Nuestros doctores</h5>
      </div>
    </div>

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
  .btn-promocion{
    border: 1px solid black;
    margin-left: 10px;
  }
  .btn-promocion:hover{
    color: white !important;
    background-color: rgb(46, 188, 158);
  }

  /* Estilo para nuestro equipo */
  .nuestroEquipo{
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    gap: 3px;
    height: 30vh;
    /* font-size: 1.5em; */
    flex-wrap: wrap;
  }

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
  grid-template-columns: 1fr 2fr; /* Una columna más pequeña y otra más grande */
}

/* mapa */
#map { height: 280px; }
</style>
 