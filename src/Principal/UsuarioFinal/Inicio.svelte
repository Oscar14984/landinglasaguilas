<script>
import Banners from "../../Componentes/Banners.svelte";
</script>

<main>
    <Banners />
    <button class="btn agenda">
      <i class="bi bi-whatsapp"></i>
      Agenda tu Primera Cita Gratis
    </button>
    <div class="tratamientos">
      <h1>TRATAMIENTOS</h1>
      <h2>Conoce nuestros Tratamietos</h2>
      <p>Todos nuestros tratamientos y servicios se brindan en cómodas instalaciones con los más altos estándares de calidad.</p>
    </div>
</main>

<style>
/* COLOR QUE SE USA EN lCD #5EBCD6 */
  .agenda{
    background-color:#5EBCD6;
    color: white;
    margin-right: 10px;
  }
  .tratamientos{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    gap: 3px;
  }
  .tratamientos h1 {
    font-size: 48px;
  }
  .tratamientos h2 {
    text-align: center;
    width: 70%;
    border-bottom: 2px solid #5EBCD6;
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
</style>
 