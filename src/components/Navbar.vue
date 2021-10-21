<template>
  <div>
    <nav class="navbar container mt-2">
      <div>
        <a class="navbar-brand" href="/">
          <img
            src="https://res.cloudinary.com/ddegh9xqy/image/upload/v1632377670/Logo_Mesa_de_trabajo_1_in9ycy.png"
            alt="Logo Inalfez"
            class="logo"
          />
        </a>
      </div>

      <div
        class="d-none d-lg-grid align-items-center"
        style="grid-template-columns: 1fr auto">
        <ul class="d-flex text-end align mb-0 justify-content-evenly" style="width: 100%">
          <li class="nav-item li-nav my-lg-0">
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
        <button type="button" class="btn btn-primary paga d-none d-lg-block">
          Paga tu crédito
        </button>
      </div>

      <div class="navbar-sidebar-button d-lg-none">
        <div>
          <label for='collapsable' class='button'><Menu /></label>
        </div>
      </div>
    </nav>
  </div>
</template>
<script>

import Menu from './icons/Menu.vue'

export default {
  name: 'Navbar',

  components: {
    Menu,
  }
}
</script>
<style scoped>
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
  transition: 0.3s;
}

.li-nav a:hover {
  color: white !important;
  transform: scale(1.1);
  font-weight: bold;
}

.li-nav a:focus {
  color: white;
}

.navbar-sidebar-button {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: end;
  align-items: center ;
}

.navbar-sidebar-button div {
  width: max-content;
  height: max-content;
}

.button {
    cursor: pointer;
    font-weight: 800;
    color: black;
    font-size: 40px;
  }
</style>