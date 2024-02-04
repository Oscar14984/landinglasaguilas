<script>
    let doctorsData = [
      { imgSrc: 'img/Dr-Juan-Carlos.png', title: 'ESPECIALISTA EN IMPLANTOLOGÍA', name: 'Dr. Juan Carlos V.' },
      { imgSrc: 'img/Dr-Miguel-Angel.jpg', title: 'ESPECIALISTA EN ENDODONCIA', name: 'Dr. Miguel Ángel S.' },
      { imgSrc: 'img/Dr-Javier-Serrano.png', title: 'DIRECTOR LA CLÍNICA DENTAL SANTA FE', name: 'Dr. Javier S.' },
      // Agrega más datos según sea necesario
    ];
  
    // Agrupar los datos en conjuntos de tres
    let groupedDoctors = [];
    for (let i = 0; i < doctorsData.length; i += 3) {
      groupedDoctors.push(doctorsData.slice(i, i + 3));
    }
  </script>
  
  <main>

      <div id="doctorCarousel" class="carousel slide" data-ride="carousel">
        <div class="carousel-inner">
          {#each groupedDoctors as group, groupIndex}
            <div class="carousel-item {groupIndex === 0 ? 'active' : ''}">
              <div class="row">
                {#each group as doctor, doctorIndex}
                  <div class="col-sm-4">
                    <div class="card">
                      <!-- svelte-ignore a11y-img-redundant-alt -->
                      <img class="card-img-top" src={doctor.imgSrc} alt="Card image cap">
                      <div class="card-body">
                        <h5 class="card-title">{doctor.title}</h5>
                        <p class="card-text">{doctor.name}</p>
                      </div>
                    </div>
                  </div>
                {/each}
              </div>
            </div>
          {/each}
        </div>
      
        <a class="carousel-control-prev" href="#doctorCarousel" role="button" data-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="sr-only">Previous</span>
        </a>
        <a class="carousel-control-next" href="#doctorCarousel" role="button" data-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="sr-only">Next</span>
        </a>
      </div>
  </main>
  