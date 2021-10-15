<template>
  <div id="app" class="position-relative d-flex align-items-center flex-column">
        <div class="fondo-general">
            <!--
        <div class="position-absolute fondo-general">
          
            <img src="https://res.cloudinary.com/ddegh9xqy/image/upload/v1632436541/fondo_landing_ifeazb.png" alt="Fondo" class="fondo1">
          
        </div>-->

            <!-- Nav -->

            <nav class="navbar container pt-4">
                <div>
                    <a class="navbar-brand" href="/">
                        <img src="https://res.cloudinary.com/ddegh9xqy/image/upload/v1632377670/Logo_Mesa_de_trabajo_1_in9ycy.png" alt="Logo Inalfez" class="logo">
                    </a>
                </div>

                <div class="d-lg-grid align-items-center" style="grid-template-columns: 1fr auto;">
                    <ul class="d-flex text-end align mb-0 justify-content-evenly" style="width: 100%;">
                        <li class="nav-item li-nav my-lg-0 ">
                            <a class="" href="">¿Quiénes somos?</a>
                        </li>
                        <li class="nav-item li-nav my-lg-0">
                            <a class="" href="">La Reserva</a>
                        </li>
                        <li class="nav-item li-nav my-lg-0">
                            <a class="" href="">Nuestro Equipo</a>
                        </li>
                        <li class="nav-item li-nav my-lg-0">
                            <a class="" href="">Contáctanos</a>
                        </li>
                    </ul>
                    <button type="button" class="btn btn-primary paga d-none d-lg-block">Paga tu crédito</button>
                </div>

                <NavbarColapsable></NavbarColapsable>
            </nav>

            <!-- Portada -->

            <div class="container mt-5">
                <div class="row">
                    <div class="col-6 info">
                        <h3 class="mb-0">El lugar perfecto para</h3>
                        <h2 class="mb-2">LA FAMILIA</h2>
                        <button type="button" class="btn btn-primary saber">Quiero saber más</button>
                    </div>
                    <div class="col-6 img">
                        <img src="https://res.cloudinary.com/ddegh9xqy/image/upload/v1632381164/familia_ao6edf.png" alt="Familia" class="familia">
                    </div>
                </div>
            </div>

        </div>

        <!-- ¿Quiénes somos? -->

        <div class="container quienes d-none d-lg-block">
            <div class="row justify-content-center">
                <div class="col-4" style="width: 300px;">
                    <div class="row row-cols-1">
                        <div class="col">
                            <img src="https://res.cloudinary.com/ddegh9xqy/image/upload/v1632465595/WhatsApp_Image_2021-08-20_at_11.04.56_AM_1_fwacmf.jpg" alt="" class="img-quienes">
                        </div>
                        <div class="col">
                            <h2>¿Quiénes somos?</h2>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit provident corporis delectus perspiciatis, voluptatibus doloribus cum accusamus earum. Eum rerum, maxime labore ipsa quibusdam vel quaerat odio perferendis in
                                ea.
                            </p>
                            <span>Ver más...</span>
                        </div>
                    </div>
                </div>
                <div class="col-4" style="width: 300px;">
                    <div class="row row-cols-1">
                        <div class="col">
                            <img src="https://res.cloudinary.com/ddegh9xqy/image/upload/v1632465595/WhatsApp_Image_2021-08-20_at_11.04.56_AM_1_fwacmf.jpg" alt="" class="img-quienes">
                        </div>
                        <div class="col">
                            <h2>Misión</h2>
                            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Distinctio dolores nesciunt tenetur minima voluptate molestias nemo veritatis cupiditate in eos enim sint iusto, optio, eligendi facilis maiores quas necessitatibus
                                officiis!
                            </p>
                            <span>Ver más...</span>
                        </div>
                    </div>
                </div>
                <div class="col-4" style="width: 300px;">
                    <div class="row row-cols-1">
                        <div class="col">
                            <img src="https://res.cloudinary.com/ddegh9xqy/image/upload/v1632465595/WhatsApp_Image_2021-08-20_at_11.04.56_AM_1_fwacmf.jpg" alt="" class="img-quienes">
                        </div>
                        <div class="col">
                            <h2>Visión</h2>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis possimus autem pariatur placeat consectetur! Rem saepe earum a mollitia labore, soluta quis! Nihil eum, tempore vel natus excepturi labore officiis.</p>
                            <span>Ver más...</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="quienesSomos-container d-flex flex-column mb-5 d-lg-none">
            <div class="swiper quienesSomos p-0">
                <div class="swiper-wrapper">
                    <div class="swiper-slide">
                        <div class="" style="width: 300px;">
                            <div class="row row-cols-1">
                                <div class="col">
                                    <img src="https://res.cloudinary.com/ddegh9xqy/image/upload/v1632465595/WhatsApp_Image_2021-08-20_at_11.04.56_AM_1_fwacmf.jpg" alt="" class="img-quienes">
                                </div>
                                <div class="col text-start">
                                    <h2>¿Quiénes somos?</h2>
                                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit provident corporis delectus perspiciatis, voluptatibus doloribus cum accusamus earum. Eum rerum, maxime labore ipsa quibusdam vel quaerat odio perferendis
                                        in ea.
                                    </p>
                                    <span>Ver más...</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="swiper-slide">
                        <div class="" style="width: 300px;">
                            <div class="row row-cols-1">
                                <div class="col">
                                    <img src="https://res.cloudinary.com/ddegh9xqy/image/upload/v1632465595/WhatsApp_Image_2021-08-20_at_11.04.56_AM_1_fwacmf.jpg" alt="" class="img-quienes">
                                </div>
                                <div class="col text-start">
                                    <h2>Misión</h2>
                                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit provident corporis delectus perspiciatis, voluptatibus doloribus cum accusamus earum. Eum rerum, maxime labore ipsa quibusdam vel quaerat odio perferendis
                                        in ea.
                                    </p>
                                    <span>Ver más...</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="swiper-slide">
                        <div class="" style="width: 300px;">
                            <div class="row row-cols-1">
                                <div class="col">
                                    <img src="https://res.cloudinary.com/ddegh9xqy/image/upload/v1632465595/WhatsApp_Image_2021-08-20_at_11.04.56_AM_1_fwacmf.jpg" alt="" class="img-quienes">
                                </div>
                                <div class="col text-start">
                                    <h2>Visión</h2>
                                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit provident corporis delectus perspiciatis, voluptatibus doloribus cum accusamus earum. Eum rerum, maxime labore ipsa quibusdam vel quaerat odio perferendis
                                        in ea.
                                    </p>
                                    <span>Ver más...</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- <div class="proyecto d-flex justify-content-center">
            <div class="fondo"></div>
            <div class="proyecto-p1">
                <div class="img-p1">
                </div>
                <div class="info-p1"></div>
            </div>
        </div> -->

        <div class="equipo d-flex flex-column mb-5">
            <div class="team-title d-flex justify-content-center align-items-center py-5 mb-5 mb-md-0">
                <p>Nuestro equipo</p>
            </div>
            <div class="swiper personal">
                <div class="swiper-wrapper">
                    <div class="swiper-slide">
                        <div class="team-card d-flex flex-column">
                            <div class="team-img d-flex justify-content-center">
                                <div></div>
                            </div>
                            <div class="d-flex flex-column align-items-center my-auto" style="height: 100%;">
                                <p style="font-size: 18px;"><strong>Gabriel Alferez</strong> - CEO INALFEZ S.A.S</p>
                                <p style="font-size: 14px;">“Amo mi trabajo como si fuera mi vida”</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="d-none d-md-block">
                    <div class="swiper-button-next"></div>
                    <div class="swiper-button-prev"></div>
                </div>
            </div>
        </div>

        <div class="footer mt-5"></div>

    </div>
</template>

<script>

export default {
  name: "App",
  components: {
  },
};

new Swiper(".personal", {
    effect: "flip",
    grabCursor: true,
    loop: true,
    autoplay: {
        delay: 5000,
        disableOnInteraction: false,
    },
    pagination: {
        el: ".swiper-pagination",
    },
    navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev",
    },
});

new Swiper(".quienesSomos", {
    spaceBetween: 30,
    centeredSlides: true,
    loop: true,
    autoplay: {
        delay: 2500,
        disableOnInteraction: false,
    },
    pagination: {
        el: ".swiper-pagination",
        clickable: true,
    },
    navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev",
    },
});
</script>

<style>
#app {
  font-family: 'Poppins', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;
  padding: 0;
}

.footer {
    width: 100%;
    height: 500px;
    background-color: #0d6efd;
}

    .quienesSomos-container {
        width: 100%;
        height: max-content;
    }
    
    .quienesSomos {
        width: 300px;
        height: max-content;
    }
    
    .quienesSomos .swiper-wrapper .swiper-slide {
        width: 100%;
        height: max-content;
        display: flex;
        text-align: center;
        font-size: 18px;
        background: #fff;
    }
    
    .quienesSomos .col {
        padding: 0 25px;
    }
    
    .quienesSomos h2 {
        font-size: 25px;
        margin-top: 15px;
        font-weight: 700;
    }
    
    .quienesSomos p {
        -webkit-box-orient: vertical;
        -webkit-line-clamp: 3;
        display: -webkit-box;
        font-size: 14px;
        overflow: hidden;
        text-align: left;
    }
    
    .quienesSomos span {
        font-size: 14px;
        color: #94C11E;
        font-weight: 500;
    }

.equipo {
    width: 100%;
    height: 1080px;
    display: flex;
    justify-content: center;
    background-image: url('./assets/fondo-equipo.jpeg');
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
}

@media (max-width: 1600px) {
    .equipo {
        height: 900px;
    }
}

@media (max-width: 1300px) {
    .equipo {
        height: 768px;
    }
}

@media (max-width: 1000px) {
    .equipo {
        height: 600px;
    }
}

@media (max-width: 800px) {
    .equipo {
        background: none;
    }
}

.swiper {
    width: 500px;
    height: 400px;
    padding: 50px;
}

.swiper-slide {
    background-position: center;
    background-size: cover;
    width: 400px;
    height: 300px;
}

.button-container {
    width: 40px;
    height: 40px;
    border-radius: 50%;
}

.team-title p {
    font-size: 25px;
    font-weight: bold;
}

.team-card {
    width: 100%;
    height: 300px;
    background-color: white;
    box-shadow: 0px 3px 8px -1px rgba(0, 0, 0, 0.5);
    border-radius: 20px;
}

.team-img div {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    position: relative;
    top: -30px;
    background-image: url('https://www.dzoom.org.es/wp-content/uploads/2020/02/portada-foto-perfil-redes-sociales-consejos.jpg');
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
}

@media (max-width: 768px) {
    .swiper {
        width: 450px;
        height: 350px;
        padding: 0;
    }

    .swiper-slide {
        width: 100%;
        height: 100%;
    }

    .team-card {
        height: 100%;
    }

    /* .team-img div {
        width: 150px;
        height: 150px;
    } */
}

@media (max-width: 500px) {
    .swiper {
        width: 320px;
        height: 250px;
    }

    .team-img div {
        width: 100px;
        height: 100px;
    }

    .team-img div {
        width: 150px;
        height: 150px;
    }
}

.navbar {
    height: 60px;
    display: grid;
    grid-template-columns: auto 1fr;
}

.logo {
    max-width: 150px;
}

.paga {
    width: 160px;
    font-size: 14px !important;
    padding: 8px 25px !important;
    box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
    -webkit-box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
    -moz-box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
}

.nav-item {
    font-size: 15px;
    margin: 0 5px;
}

.nav-item,
.nav-item a {
    text-decoration: none;
    list-style: none;
}

.nav-item a {
    color: white;
    font-weight: 400;
    text-shadow: 2px 2px 5px rgb(31, 31, 31);
    transition: .3s;
}

.li-nav a:hover {
    color: white !important;
    transform: scale(1.1);
    font-weight: 700px;
}

.li-nav a:focus {
    color: white;
}

@media (max-width: 992px) {
    .navbar-colapsable {
        height: 100vh;
        position: fixed;
        top: 0;
        right: 0;
        background-color: white;
        z-index: 102;
        transition: all .5s;
    }
    .navbar-colapsable ul a {
        font-weight: bold;
        color: #007aff;
        text-shadow: none;
    }
}

html {
    font-size: 62.5%;
}

.blanco {
    background: white;
    width: 185px;
    height: 80px;
    left: -2px;
    border-radius: 0 0 25px 25px;
    z-index: -99;
}

.contenedor {
    max-width: 1080px;
    width: 100%;
    padding: 0 20px;
}

.contenedor .row {
    height: 100%;
}

.quienes {
    margin-bottom: 80px;
}

.quienes .col {
    padding: 0 25px;
}

.quienes h2 {
    font-size: 25px;
}

.fondo-general {
    background: url("https://res.cloudinary.com/ddegh9xqy/image/upload/v1632982503/fondo_landing_wbmqbx.png");
    width: 100%;
    max-width: 1920px;
    height: 780px;
    background-size: cover;
}

.fondo1 {
    padding-top: 180px;
    margin: auto;
    width: 100%;
    max-width: 1920px;
}

.info {
    display: flex;
    flex-direction: column;
    color: white;
    justify-content: center;
    padding-bottom: 100px;
}

.info h3 {
    font-size: 30px;
    text-shadow: 2px 2px 5px rgb(31, 31, 31);
}

.info h2 {
    font-size: 80px;
    font-weight: 800;
    text-shadow: 2px 2px 10px rgb(31, 31, 31);
}

.saber {
    font-size: 14px !important;
    padding: 10px 25px !important;
    box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
    -webkit-box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
    -moz-box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
    width: 200px;
    border-radius: 100px !important;
}

.img {
    display: flex;
    justify-content: center;
    align-items: flex-end;
    padding: 10px;
}

.img img {
    width: 100%;
    max-width: 425px;
}

.quienes h2 {
    margin-top: 15px;
    font-weight: 700;
}

.quienes p {
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 3;
    display: -webkit-box;
    font-size: 14px;
    overflow: hidden;
    text-align: left;
}

.quienes span {
    font-size: 14px;
    color: #94C11E;
    font-weight: 500;
}

.img-quienes {
    width: 100%;
    border-radius: 20px;
}

.proyecto .fondo {
    position: absolute;
    background-image: url("https://res.cloudinary.com/ddegh9xqy/image/upload/v1633466174/fondo_yayuma.svg");
    width: 100%;
    max-width: 1920px;
    height: 780px;
    background-size: cover;
    z-index: 0;
}

.proyecto-p1 {
    z-index: 100;
}

.img-p1 {
    height: 100%;
    width: 370px;
    background-image: url("https://res.cloudinary.com/ddegh9xqy/image/upload/v1633467938/foto_1_jvjen2.png");
    background-size: cover;
}
</style>
