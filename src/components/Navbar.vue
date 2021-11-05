<template>
  <header id="head">
            <a href="#" class="izquierda">
                <div class="logo">
                    <img src="https://res.cloudinary.com/ddegh9xqy/image/upload/v1632377670/Logo_Mesa_de_trabajo_1_in9ycy.png" alt="Logo">
                </div>
            </a>


            <ul :class="menu">
                <div class="salir" v-on:click="toggleCollapsed">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M11 17l-5-5m0 0l5-5m-5 5h12" />
                    </svg>
                </div>

                <a href="#inicio" v-on:click="toggleCollapsed">
                    <li>¿Quiénes somos?</li>
                </a>
                <a href="#quienes" v-on:click="toggleCollapsed">
                    <li>La Reserva</li>
                </a>
                <a href="#expor" v-on:click="toggleCollapsed">
                    <li>Galeria</li>
                </a>
                <a href="#certifi" v-on:click="toggleCollapsed">
                    <li>Contáctanos</li>
                </a>
                <button type="button" class="btn btn-primary paga">
          Paga tu crédito
        </button>
            </ul>
            <div class="menu__movil d-block d-lg-none" v-on:click="toggleCollapsed">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                </svg>
            </div>



        </header>
</template>
<script>
export default {
  name: 'Navbar',
data() {
  return {
    isCollapsed: true,
  }
},

methods:{
toggleCollapsed() {
            this.isCollapsed = !this.isCollapsed
        },

},

  computed: {
        menu() {
            if (this.isCollapsed) {
                return "nav collapsed"
            }
            return "nav"
        },
  }




}





</script>
<style scoped>
  header{
    max-width: 1080px;
    margin: auto;
    display: flex;
    align-items: center;
    padding: 15px 20px;
    justify-content: space-between;
}

.paga {
  margin-left: 20px;
  width: 160px;
  font-size: 14px !important;
  padding: 8px 25px !important;
  box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
  -webkit-box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
  -moz-box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
  border-radius: 60px;
}

.izquierda{
    display: flex;
    align-items: center;
    text-decoration: none;
    color: var(--negro);
}

.logo img {
    max-width: 150px;
}

.nav {
    display: flex;
    align-items: center;
}

.nav a{
    text-decoration: none;
    color: #ffffff ;
    color: white;
    font-weight: 400;
    text-shadow: 2px 2px 5px rgb(31, 31, 31);
    transition: 0.3s;
}

.nav li {
    font-size: 16px;;
    margin-left: 20px;
    list-style: none;
}

.nav li:hover {
    color: var(--verde_oscuro);
}

.menu__movil svg{
    width: 0px;
    color: #0d6efd;
}

.salir {
    margin-right: auto;
}

.salir svg{
    display: none;
}

.op{
    display: none;
}

.arriba{
    display: flex;
    position: fixed;
    bottom: 25px;
    right: 25px;
    z-index: 90;
    background-color: var(--verde_oscuro);
    padding: 10px;
    border-radius: 50%;
    transition: all 300ms ;
    opacity: 0;
}

.arriba svg{
    color: #fff;
    width: 30px;
    height: 30px;
}

.arriba:hover{
    background-color: var(--verde_claro); 
	box-shadow: 0px 15px 20px rgba(0, 0, 0, 0.3);
	transform: translateY(-7px);
}

.show{
    transition: all 300ms ;
    opacity: 100%;
}


.english{
    display: flex;
    position: absolute;
    top: 30px;
    right: 0;
    background-color: #fff;
    border-radius: 10px;
    padding: 10px 25px;
    box-shadow:  20px 20px 60px #bebebe,
    20px -20px 60px #ffffff;
}

.nada{
    display: none;
}



@media (max-width:992px){


    .paga{
        border-radius: 5px;
    }

    .nav{
        padding: 20px;
        background-color: white;
        position: fixed;
        right: 0;
        top: 0;
        height: 100%;
        width: 250px;
        flex-direction: column;
        align-items: flex-end;
        z-index: 99;
        transition: all .5s;
        box-shadow:
        15px -15px 30px #636363
    }

    .op{
        margin-top: 50px;
        display: block;
        order: 9;
        font-size: 16px;
        color: var(--verde_oscuro);
        font-weight: 700;
    }


    .idioma{
        margin: 5px 0;
        order: 10;
    }

    .nav a{
    text-decoration: none;
    color: #636363 ;
    text-shadow: none;
}

    .nav li{
        margin: 12px 0;
    }

    .collapsed{
        transition: all 1.5s;
        right: -100%;
    }


    .menu__movil svg{
        width: 30px;
    }

    .salir svg{
        display: block;
        width: 30px;
        height: 30px;
        transition: all 1s;
        margin-bottom: 10px;
        color: #0d6efd;
    }
}

@media (max-width: 375px){

    .orgullo{
        margin-left: 10px;
    }

    .orgullo p{
        font-size: 12px;
    }

    .orgullo strong{
        font-size: 20px;
    }

}
</style>