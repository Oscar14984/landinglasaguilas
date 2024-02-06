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
    <div class="renueva" style="margin-bottom: 20px;">
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
      </div>
      <div id="map">
        <Mapa />
      </div>
    </div>
    

    <!-- INFORMACION DE CONTACTO -->
    <div class="contactos">
      <img src="img/informacion.png" alt="">
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
  border-radius: 50%;
  width: 100px; 
  height: 100px; 
  object-fit: cover; 
}

/* ESTILOS DE RENOVACION */
.renueva{
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  padding: 10px;
  background: linear-gradient(to left, #5EBCD6, white); 
}

.ren-son{
  margin-right: 200px;
}

/* ESTILO DE LA INSTALACION */
.instalaciones {
  display: flex;
  justify-content: space-between; 
  align-items: center; 
  margin-bottom: 40px;
  margin-left: 30px; 
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
    
  }
  .btn-insta:hover{
    color: white !important;
    background-color: rgb(46, 188, 158);
  }

/* ESTILOS PARA EL FORMS Y EL MAPA  */
.map-forms {
  display: flex;
}

.forms {
  flex: 1; /* El texto ocupa todo el espacio disponible */
}

#map {
  flex: 1; /* El mapa ocupa todo el espacio disponible */
}
.forms {
  flex: 1;
  padding-right: 20px; /* Añade un espacio entre el formulario y el mapa */
}

.contacto {
  background-color: #f8f9fa; /* Color de fondo para los campos de formulario */
  padding: 20px;
  border-radius: 10px; /* Añade esquinas redondeadas al formulario */
}

.form-label {
  font-weight: bold; /* Hace que las etiquetas de los campos de formulario sean más visibles */
}

.form-control {
  width: 100%; /* Ajusta el ancho de los campos de formulario */
  margin-bottom: 10px; /* Añade espacio entre los campos */
}

textarea.form-control {
  resize: vertical; /* Hace que el área de texto se pueda redimensionar verticalmente */
}

.inputs {
  display: flex;
  justify-content: space-between; /* Distribuye los elementos a los extremos */
}


/* mapa */
#map { height: 500px; }
</style>
 