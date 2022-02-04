<template>
<div>
    <div class="row container justify-content-center align-items-center vender" >
        <div class="d-flex col-lg-5 col-auto flex-column px-4">
            <h3>¿Estás entusiasmado y quieres comprar ya?</h3>
            <p>Da clic en el siguiente botón e inicia un chat con una asesora de ventas para que te guíe en el proceso de compra del lote. <br> <span class="sub"> ¡Construye el patrimonio de tu futuro y el de tus seres queridos ahora!</span></p>
        </div>
        <div class="d-flex col-auto">
            <a class="ayuda" href="https://wa.link/52o2i7" target="a_blank">Necesito asesoría</a>
        </div>
    </div>

    <div class="row container justify-content-center align-items-center vender" >
        <div class="d-flex col-lg-5 col-auto flex-column px-4">
            <h3>¿Quiéres tener un mejor plano de nuestro proyecto?</h3>
            <p>Da clic en el siguiente botón y comienza a ver la mejor inversión para tu futuro. <br> <span class="sub"> ¡Construye el patrimonio de tu futuro y el de tus seres queridos ahora!</span></p>
        </div>
        <div class="d-flex col-auto">
            <a class="ayuda" href="https://drive.google.com/file/d/1IL7W3OgLz2bVpKDDIVjcFksGwQdlLmB1/view?usp=sharing" target="a_blank">Ver mapa</a>
        </div>
    </div>
</div>
</template>
<script>
export default {
name: "Equipo",

data() {
return {
    modal: false,
    quienes: "",
        };
    }
};
</script>
<style scope>

.vender{
    margin-top: 100px;
}

p{
    font-size: 14px;
}

.sub{
    font-weight: 600;
}

.ayuda{
    padding: 10px 30px;
    background: #70C217;
    font-size: 14px;
    color: white;
    border-radius: 50px;
    text-decoration: none;
    margin-left: 50px;
    transition: .3s;
    box-shadow: -10px 12px 23px -11px rgb(57 57 57 / 67%);
    -webkit-box-shadow: -10px 12px 23px -11px rgb(57 57 57 / 67%);
    -moz-box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
    cursor: pointer;
}

.ayuda:hover{
    color: white;
    transform: scale(1.1);
}

.modal-mision {
width: 100vw;
height: 100vh;
display: flex;
justify-content: center;
align-items: center;
position: fixed;
top: 0;
left: 0;
background: rgba(0, 0, 0, 0.5);
transition: all 500ms ease;
opacity: 1;
z-index: 1000;
}

.modal-mision .contenedor-mision {
width: 50%;
height: 400px;
padding: 20px;  
margin: auto;
border-radius: 20px;
background: #fff;
box-shadow: 1px 7px 25px rgba(0, 0, 0, 0.288);
transition: all 500ms ease;
position: relative;
transform: translateY(-30%);
}

@media (max-width:992px) {
    .ayuda{
        margin-left: 0px;
        margin-top: 10px;
    }

    .vender{
        margin-top: 75px;
    }
}

</style> 