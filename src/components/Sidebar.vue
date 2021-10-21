<template>
  <input type='checkbox' id='collapsable' class="d-none">
  <div class="sidebar">
    <div class="sidebar-content">
      <div class="close-sidebar-container mb-5">
        <label for="collapsable" class="close-sidebar">
          <ChevronRight />
        </label>
      </div>

      <div>
        <div>
          <ul class="d-flex flex-column text-end" style="width: 100%">
            <li class="nav-item li-nav mb-5">
              <a class="" href="">¿Quiénes somos?</a>
            </li>
            <li class="nav-item li-nav mb-5">
              <a class="" href="">La Reserva</a>
            </li>
            <li class="nav-item li-nav mb-5">
              <a class="" href="">Nuestro Equipo</a>
            </li>
            <li class="nav-item li-nav mb-5">
              <a class="" href="">Contáctanos</a>
            </li>
          </ul>
        </div>

        <div class="d-flex justify-content-end">
          <button type="button" class="btn btn-primary paga">
            Paga tu crédito
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ChevronRight from './icons/ChevronRight.vue'

export default {
  name: "Sidebar",
  components: {
    ChevronRight,
  },
  
};
</script>

<style scoped>
.sidebar {
  width: 0;
  height: 100vh;
  top: 0;
  right: 0;
  position: fixed;
  background-color: white;
  transition: 0.3s;
}

.sidebar .sidebar-content {
  display: none;
}

.close-sidebar-container {
  width: 100%;
  height: 60px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.close-sidebar {
  width: max-content;
  height: max-content;
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
  color: #0d6efd;
  font-weight: bold;
  transition: 0.3s;
}

.paga {
  width: 160px;
  font-size: 14px !important;
  padding: 8px 25px !important;
  box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
  -webkit-box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
  -moz-box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
}

#collapsable:checked + .sidebar {
  width: 250px;
  height: 100vh;
  padding-left: 20px;
  padding-right: 20px;
  position: fixed;
  top: 0;
  right: 0;
  z-index: 102;
  transition: 0.3s;
  background-color: white;
  border-right: 1px solid #E5E7EB;
  display: grid;
  grid-template-rows: auto 1fr;
}

#collapsable:checked + .sidebar .sidebar-content {
  display: block;
  transition: 0.3s;
}

</style>
