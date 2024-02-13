<script>
let horas = "9:00AM - 7:00PM"
</script>

<main>
    <div class="contacto-principal">
        <h1>Contactanos</h1>
        <div class="contenido-p-contacto-principal">
            <p>Llámanos 5589003683 y consigue ¡la sonrisa de tus sueños!</p>
        </div>
    </div>
    <div class="contacto-direccion">
       <div class="row">
        <div class="col">
            <div class="direccion">
                <strong>La Clínica Dental las Aguilas</strong>
                <div>
                    <a href="https://www.google.com.mx/maps/place/Anillo+Perif.+2165,+Los+Alpes,+%C3%81lvaro+Obreg%C3%B3n,+01010+Ciudad+de+M%C3%A9xico,+CDMX/@19.3606707,-99.1937018,18z/data=!3m1!4b1!4m6!3m5!1s0x85d2002033c9fd49:0x34e5689b3d509582!8m2!3d19.3606682!4d-99.1924143!16s%2Fg%2F11kbwmmnn0?entry=ttu" target="_blank">Anillo Perif. 2165, Los Alpes, Álvaro Obregón.</a>
                </div>
                <strong>¡Escríbenos!</strong>
                <div>
                    <p>contacto@laclinicalasaguilas.dental</p>
                </div>
            </div>
        </div>
        <div class="col">
            <div class="horarios">
                <div class="d">
                    <p>Lunes </p> 
                    <p>Martes </p>
                    <p>Miercoles </p>
                    <p>Jueves </p>
                    <p>Viernes </p>
                    <p>Sabado </p>
                </div>
                <dir class="h">
                    <p>{horas}</p>
                    <p>{horas}</p>
                    <p>{horas}</p>
                    <p>{horas}</p>
                    <p>{horas}</p>
                    <p>{horas}</p>
                </dir>
            </div>
        </div>

       </div>
    </div>
</main>

<style>
.contacto-principal{
    text-align: center;
    padding: 50px 50px;
    background-image: url(img/fondo.jpg);
    background-size: 70%;
    background-repeat: no-repeat; 
    background-position: center top ; 
    margin: 50px 50px 40px 40px;
    color: white;
   font-size: 2rem;
}

.direccion {
        /* text-align: center; */
        background-color: #b969de89;
        padding-bottom: 18.5%;
        margin-left: 50px;

    }

    .direccion strong {
        display: block;
        margin-bottom: 5px;
        text-align: end;
        margin-right: 20px;
    }

    .direccion a {
        display: block;
        text-decoration: none;
        text-align: end;
        margin-bottom: 10px;
        border-bottom: 2px solid white;
        margin-right: 20px;
    }
    .direccion p{
        text-align: end;
        margin-right: 20px;
    }

    /* .direccion div:not(:last-child) {
        margin-bottom: 10px;
    } */

.horarios{
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    background-color: #2D3549;
    color:white;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin-bottom: 20px;
    margin-right: 50px;
    }

    .d {
        text-align: right;
        margin-left: 15px;
    }

    .h {
        text-align: left;
        margin-right: 15px;
    }

</style>