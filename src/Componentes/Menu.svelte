<script>
	import Inicio from './../Principal/UsuarioFinal/Inicio.svelte';
  import {link, push} from 'svelte-spa-router'

  const llamar = () => {
        window.location.href = 'tel:5589003683';
    }
    const abrirWhats = () =>{
        window.open('https://api.whatsapp.com/send/?phone=5215515101285&text=%C2%A1Hola%21+Quiero+agendar+una+Cita+de+Valoraci%C3%B3n+en+La+Cl%C3%ADnica+Dental+Coapa&type=phone_number&app_absent=0', '_blank');
    }
  const inicio = () =>{
    push('/')
  }
</script>

<main>
    <nav class="navbar navbar-expand-lg ">
        <div class="container-fluid">
          <!-- svelte-ignore a11y-click-events-have-key-events -->
          <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
          <img src="logos/Logo Horizontal[46].jpeg" alt="" on:click={inicio}>
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0 ">
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" use:link href="/">INICIO</a>
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
                <a class="nav-link" use:link href="/Contactanos">CONTÁCTANOS</a>
              </li>
              
            </ul>
            <button class="btn agenda" on:click={abrirWhats}>
                <i class="bi bi-whatsapp"></i>
                Agenda tu Primera Cita Gratis
            </button>
            <button class="btn llamada"  on:click={llamar}>
                <i class="bi bi-telephone"></i>
                Llámanos
            </button>
          </div>
        </div>
      </nav>
</main>

<style>
  img{
    cursor: pointer;
  }
/* COLOR QUE SE USA EN lCD #5EBCD6 */
.agenda {
  background-color: #5EBCD6;
  color: white;
  margin-right: 5px; 
  font-size: 14px; 
  padding: 5px 10px; 
}

.llamada {
  background-color: #5EBCD6;
  color: white;
  font-size: 14px; 
  padding: 5px 3px; 
}
.nav-item a{
  color: #dc0beb;
}
  /* HOVER DEL nav-item a */
  .navbar-nav{
    margin-left: 27%;
  }
  .navbar-nav .nav-item.active a,
  .navbar-nav .nav-item:hover a {
    color: #5EBCD6; 
    border-bottom: 2px solid #5EBCD6; 
  }

  .navbar-expand-lg{
    position: fixed;
    left: 0;
    top: 0;
    width: 100%;
    background-color: rgba(149, 230, 255, 0.9);
    /* color: white; */
    text-align: center;
    z-index: 1;
  }
  /* Estilos para el logo en la barra de navegación */
.navbar img {
  /* max-width: 100%;  */
  /* height: auto;  */
  width: 15%;
  margin-right: 10px; 
}

/* Media query para ajustar el tamaño del logo en dispositivos móviles */
@media screen and (max-width: 767px) {
  .navbar img {
    max-width: 80px; 
  }
}
</style>
