<template>
    <div class="container" id="simulador">
        <h2 class="titulo">¡Simula tu reserva!</h2>
        <div class="row p-5">
            <form class="col-lg-6 col-auto d-flex  flex-column padding formu" @submit.prevent="onSubmit">
                <input v-model="nombre" class="input" placeholder="Nombre completo">
                <!-- <p style="color: red; text-align: start;" v-if="this.alertNombre">Este campo es requerido para simular.</p> -->
                <input v-model="correo" class="input" type="email" placeholder="Correo electronico">
                <input v-model="numero" class="input" type="number"  id="tel" name="tel" placeholder="Número de WhatsApp">

                <select  v-model="currentLote"  class="form-select input" placeholder="Lote de interés">
                    <option disabled selected value="">Lote de interés</option>
                    <option v-for="item in lotes" :key="item.id">{{item.lote}}</option>
                </select>

                <select  v-model="meses" class="form-select input" placeholder="Meses a financiar">
                    <option disabled selected value="">Meses a financiar</option>
                    <option v-for="item in numMeses" :key="item.id">{{item.mes}}</option>
                </select>
                <select v-model="reserva" class="form-select input">
                    <option disabled selected value="">Tipo de reserva</option>
                    <option value="true">Con cuota inicial</option>
                    <option value="false">Sin cuota inicial</option>
                </select>
                <input v-if="reserva==='true'" v-model="cuota" type="number" class="input" placeholder="Ingresa el valor de la cuota inicial">
                <div class="d-flex mt-5 sel align-items-center">
                <input class="form-check-input " type="checkbox" value="" id="flexCheckDefault">
                <label class="form-check-label " for="flexCheckDefault">
                    Aceptar los <span class="terminos">terminos y condiciones</span> 
                </label>
                </div>
                <div>
                <button @click="simular" type="button" class="btn btn-primary mt-5">Simular</button>
                </div>
            </form>
            <div class="col-lg-6 col-auto d-flex flex-column align-items-start tabla padding">
                <div class="informacion">
                    <div class="item">
                        <h5>Lote de interes</h5>
                        <p>{{viewLote}}</p>
                    </div>
                    <div class="item">
                        <h5>Metro cuadrados</h5>
                        <p>{{objectLote.metros}}</p>
                    </div>
                    <div class="item">
                        <h5>Valor del lote</h5>
                        <p>{{objectLote.valor}}</p>
                    </div>
                    <div class="item">
                        <h5>Meses a financiar</h5>
                        <p>{{currentMes}}</p>
                    </div>
                    <div class="item">
                        <h5>Cuota inicial</h5>
                        <p>{{currentInicial}}</p>
                    </div>
                    <div class="item">
                        <h5>Cuota mensual</h5>
                        <p>{{currentCuota}}</p>
                    </div>
                    <div class="item">
                        <h5>Interes</h5>
                        <p>0 %</p>
                    </div>
                    <a :href="completo" target="_blank" v-if="quiero" class="item ya mt-4">Quiero mi lote YA</a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Simulador',
    data() {
        return {
            loteInteresStatus: false,

            nombre:"",
            correo:"",
            numero: null,
            currentLote:"",
            meses: '',
            reserva: '',
            
            quiero:false,
            cuota:null,
            valorLote:0,
            mensaje:false,
            lotes:[
                {
                    id:0,
                    lote:'Semicomercial',
                    valor:38000000,
                    metros:101.5,
                },
                {
                    id:1,
                    lote:'Residenciales',
                    valor:40000000,
                    metros:102
                },
                {
                    id:2,
                    lote:'Comercial',
                    valor:42000000,
                    metros:101.5
                },
                { 
                    id:3,
                    lote:'Residencial esquinero',
                    valor:45000000,
                    metros:112
                },
                { 
                    id:4,
                    lote:'Semicomercial esquinero',
                    valor:45000000,
                    metros:101.5
                },
                { 
                    id:5,
                    lote:'Comercial esquinero',
                    valor:47000000,
                    metros:101.5
                },
                { 
                    id:6,
                    lote:'Semicomercial #2 mz 3',
                    valor:55000000,
                    metros:118.76
                },
                { 
                    id:7,
                    lote:'Semicomercial esquinero B',
                    valor:87000000,
                    metros:216.36
                },
                { 
                    id:8,
                    lote:'Residencial B',
                    valor:126000000,
                    metros:313.18
                },
                { 
                    id:9,
                    lote:'Residencial esquinero B',
                    valor:130000000,
                    metros:313.18
                },
            ],
            numMeses:[
                {
                    id:0,
                    mes:1
                },
                {
                    id:1,
                    mes:2
                },
                {
                    id:2,
                    mes:3
                },
                {
                    id:3,
                    mes:4
                },
                {
                    id:4,
                    mes:5
                },
                {
                    id:5,
                    mes:6
                },
                {
                    id:6,
                    mes:7
                },
                {
                    id:7,
                    mes:8
                },
                {
                    id:8,
                    mes:9
                },
                {
                    id:9,
                    mes:10
                },
                {
                    id:10,
                    mes:11
                },
                {
                    id:11,
                    mes:12
                },
                {
                    id:12,
                    mes:13
                },
                {
                    id:13,
                    mes:14
                },
                {
                    id:14,
                    mes:15
                },
                {
                    id:15,
                    mes:16
                },
                {
                    id:16,
                    mes:17
                },
                {
                    id:17,
                    mes:18
                },
                {
                    id:18,
                    mes:19
                },
                {
                    id:19,
                    mes:20
                },
                {
                    id:20,
                    mes:21
                },
                {
                    id:21,
                    mes:22
                },
                {
                    id:22,
                    mes:23
                },
                {
                    id:23,
                    mes:24
                },
            ],
            viewLote:"--",
            currentMes:"--",
            currentInicial:"--",
            currentCuota:"--",
            objectLote:{
                valor:"--",
                metros:"--"
            }

        }
    },

    methods:{

        simular(){
            this.viewLote = this.currentLote.length ? this.currentLote : this.viewtLote;
            this.objectLote = this.lotes.find(element => {
                return  this.viewLote == element.lote
            })
            this.quiero = true
            this.currentMes = this.meses
            this.currentInicial = this.cuota
            this.resultLote = this.currentLote
            this.currentCuota = (parseInt(this.objectLote.valor) - parseInt(this.currentInicial)) / parseInt(this.currentMes)
            this.objectLote.valor = new Intl.NumberFormat('es-ES', { style: 'currency', currency: 'COP' }).format(this.objectLote.valor) 
            this.currentInicial = new Intl.NumberFormat('es-ES', { style: 'currency', currency: 'COP' }).format(this.currentInicial) 
            this.currentCuota = new Intl.NumberFormat('es-ES', { style: 'currency', currency: 'COP' }).format(this.currentCuota)
            
            this.nombre = ""
            this.correo = ""
            this.numero = ""
            this.currentLote = ""
            this.meses = ""
            this.reserva = "false"
            this.cuota = null
        },

        //  saveInfo(metros, valor){
        //     /* this.currentM2 = metros
        //     this.currentPrecio = valor */
        //     console.log(metros, valor)
        // } 

    },

    computed:{
        completo(){
            return "https://wa.me/573188353111/?text=Hola mi nombre es " + this.nombre + ". Estoy interesado/a en un lote tipo " + this.viewLote + ", cuyo valor es $" + this.objectLote.valor + ", mi aporte como cuota inicial es de $" + this.currentInicial + ", para financiar a " + this.currentMes + " meses, para contactarme mi correo es " + this.correo + " y mi numero de contacto o whatsApp es " + this.numero
        }
    }

}
</script>

<style scope>

.ya{
    background: #70C217;
    color: white;
    padding: 5px 15px;
    font-size: 16px;
    border-radius: 50px;
    text-decoration: none;
    box-shadow: -10px 12px 23px -11px rgb(57 57 57 / 67%);
    -webkit-box-shadow: -10px 12px 23px -11px rgb(57 57 57 / 67%);
    -moz-box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
    cursor: pointer;
    transition: all .3s;
}

.ya:hover{
    color: white;
    transform: scale(1.01);
}

.informacion{
    width: 100%;
}

.item{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    margin-top: 5px;
}

.item p{
    margin-bottom: 0;
    font-size: 25px;
    font-weight: bold;
}

.item h5{
    margin-bottom: 0;
    font-size: 14px;
    font-weight: 400;
}

.sel{
    padding: 0 40px ;
}

.btn{
    font-size: 16px;
    padding: 5px 60px;
    border-radius: 50px;
    box-shadow: -10px 12px 23px -11px rgb(57 57 57 / 67%);
    -webkit-box-shadow: -10px 12px 23px -11px rgb(57 57 57 / 67%);
    -moz-box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
}

    .sel input{
        width: 15px;
        height: 15px;

    }

    .sel label{
        margin-left: 25px;
        font-size: 14px;
    }

    .terminos{
        font-weight: 600;
    }


    .titulo{
        font-weight: 700;
        font-size: 25px;
    }

    .tabla{
        min-height: 575px;
        border-radius: 25px;
        background: #ffffff;
        box-shadow:  7px 7px 16px #cecece,-7px -7px 16px #f2f2f2;
        display: flex;
        justify-content: center;
    }



    .padding{
        padding: 25px 50px;
    }

    .input{
    color: rgb(85, 85, 85);
    display: flex;
    margin-top: 5px;
    justify-content: center;
    font-size: 16px;
    padding: 5px 40px; 
    outline: none;
    border-style: none;
    background-color: rgba(0, 0, 0, 0);
    border-bottom: 1px #1A5EE3 solid !important;
    height: 50px;
    width: 100%;
    }

    .input:focus{
        box-shadow: none;
    }

    @media (max-width:992px) {
        .input{
            padding: 5px;
        }

        .tabla{
            margin-top: 20px;
            width: 100%;
            padding: 25px 30px !important;
        }

        .formu{
            padding: 0 !important;
            margin-bottom: 10px;
            width: 100%;
        }

        .sel{
            padding: 0;
        }
    }
</style>