<script>
	import Inicio from './../Principal/UsuarioFinal/Inicio.svelte';
  import {link} from 'svelte-spa-router'
 

</script>

<main>
    <nav class="navbar navbar-expand-lg bg-light">
        <div class="container-fluid">
          <img src="img/logo-la-clinica-dental-oscuro.png" alt="">
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="!#">INICIO</a>
              </li>
              <!-- <li class="nav-item">
                <a class="nav-link" href="!#">NOSOTROS</a>
              </li> -->
              <li class="nav-item">
                <a class="nav-link" use:link href="/Tratamientos">TRATAMIENTOS</a>
              </li>
              <!-- <li class="nav-item">
                <a class="nav-link" href="!#">DENTISTAS</a>
              </li> -->
              <!-- <li class="nav-item">
                <a class="nav-link" href="!#">BLOG</a>
              </li> -->
              <li class="nav-item">
                <a class="nav-link" use:link href="https://laclinica.mx/contactanos/" target="_blank">CONTÁCTANOS</a>
              </li>
              
            </ul>
            <button class="btn agenda">
                <i class="bi bi-whatsapp"></i>
                Agenda tu Primera Cita Gratis
            </button>
            <button class="btn llamada">
                <i class="bi bi-telephone"></i>
                Llámanos
            </button>
          </div>
        </div>
      </nav>
</main>

<style>
    /* COLOR QUE SE USA EN lCD #5EBCD6 */
    .agenda{
        background-color:#5EBCD6;
        color: white;
        margin-right: 10px;
    }
    .llamada{
        background-color:#5EBCD6; 
        color: white;
    }

   

    /* HOVER DEL nav-item a */
    .navbar-nav .nav-item.active a,
  .navbar-nav .nav-item:hover a {
    color: #5EBCD6; /* Color de texto al seleccionar o pasar el ratón por encima */
    border-bottom: 2px solid #5EBCD6; /* Borde inferior al seleccionar o pasar el ratón por encima */
  }

  .navbar-expand-lg{
    position: fixed;
    left: 0;
    top: 0;
    width: 100%;
    background-color: rgba(149, 230, 255, 0.3);
    /* color: white; */
    text-align: center;
    z-index: 1;
  }
</style>
