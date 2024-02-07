<script>
    // Lógica JavaScript aquí si es necesario
  </script>
  
  <div class="button-container">
    <!-- Botón 1 -->
    <button><span>Facebook</span></button>
    <!-- Botón 2 -->
    <button><span>Cita</span></button>
  </div>
  
  <style>
    /* Estilos para el contenedor de los botones */
    .button-container {
      position: fixed;
      top: 50%;
      left: 10px; /* Ajusta la distancia desde el borde izquierdo */
      transform: translateY(-50%);
      display: flex;
      flex-direction: column;
      z-index: 999; /* Asegura que esté encima de otros elementos */
    }
  
    /* Estilos para los botones */
    .button-container button {
      margin-bottom: 5px; /* Espacio entre los botones */
      padding: 10px; /* Ajusta el espaciado interno */
      background-color: #5EBCD6;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      width: 40px; /* Ancho de los botones */
      height: 200px; /* Altura de los botones */
      writing-mode: vertical-lr; /* Modo de escritura vertical de izquierda a derecha */
      text-orientation: upright; /* Orientación vertical del texto */
    }
    /* .button-container button span {
        display: inline-block;
        transform: rotate(-180deg); 
        transform-origin: center; 
    } */
  
    /* Estilos al pasar el ratón por encima de los botones */
    .button-container button:hover {
      background-color: #4ba1b1;
    }
  </style>
  
  