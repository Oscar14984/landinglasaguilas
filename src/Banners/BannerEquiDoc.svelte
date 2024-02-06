<script>
  let docData = [
    { imgSrc: 'img/Dr-Javier-Serrano.png', title: 'ESPECIALISTA EN ALGO', name: 'Dr. Javier S.' },
    { imgSrc: 'img/Dr-Juan-Carlos.png', title: 'ESPECIALISTA EN OTRA COSA', name: 'Dr. Juan Carlos V.' },
    { imgSrc: 'img/Dr-Miguel-Angel.jpg', title: 'ESPECIALISTA EN ALGO MÁS', name: 'Dr. Miguel Ángel S.' },
    { imgSrc: 'img/Dr-Miguel-Angel.jpg', title: 'ESPECIALISTA EN ALGO MÁS', name: 'Dr. Miguel Ángel S.' },
    { imgSrc: 'img/Dr-Miguel-Angel.jpg', title: 'ESPECIALISTA EN ALGO MÁS', name: 'Dr. Miguel Ángel S.' },
    // Agrega más datos según sea necesario
  ];
</script>

<div id="carouselExampleIndicators" class="carousel slide" data-bs-ride="carousel">
  <div class="carousel-indicators">
    {#each Array.from({ length: 5 }) as _, index (index)}
      <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to={index} class={index === 0 ? 'active' : ''}></button>
    {/each}
  </div>
  <div class="carousel-inner">
    {#each docData as item, index (item)}
      <div class="carousel-item {index === 0 ? 'active' : ''}">
        <div class="card" style="width: 18rem;">
          <img src={item.imgSrc} class="card-img-top" alt="...">
          <div class="card-body">
            <p class="card-text">{item.title}</p>
          </div>
        </div>
      </div>
    {/each}
  </div>
  <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Previous</span>
  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Next</span>
  </button>
</div>