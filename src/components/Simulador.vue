<template>
    <div class="container">
        <h2 class="titulo">¡Simula tu reserva!</h2>
        <div class="row p-5">
            <div class="col-6 d-flex  flex-column padding">
                <input class="input" placeholder="Ingresa tu nombre completo" required>
                <input class="input" type="email" placeholder="Ingresa tu correo electronico" required>
                <input class="input" type="tel"  id="tel" name="tel" placeholder="Ingresa tu número de WhatsApp" required>

                <select  class="form-select input">
                    <option disabled selected value="">Selecciona el el lote de interés</option>
                    <option v-for="item in lotes" :key="item.id">{{item.lote}}</option>
                </select>

                <select  v-model="meses" class="form-select input" placeholder="Meses a financiar">
                    <option disabled selected value="">Selecciona los meses a financiar</option>
                    <option v-for="item in numMeses" :key="item.id">{{item.mes}}</option>
                </select>
                <select v-model="reserva" class="form-select input">
                    <option disabled selected value="">Selecciona el tipo de reserva</option>
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
            </div>
            <div class="col-6 d-flex tabla">
                
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Simulador',
    data() {
        return {
            meses: '',
            cuota:null,
            valor:0,
            valorLote:0,
            reserva: '',
            lotes:[
                {
                    id:0,
                    lote:'Residencial esquinero',
                    valor:45000000,
                    metros:105.5,
                },
                {
                    id:1,
                    lote:'Residencial ',
                    valor:45000000,
                    metros:105.6
                },
                {
                    id:2,
                    lote:'Semicomercial esquinero',
                    valor:45000000,
                    metros:105.7
                },
                { 
                    id:3,
                    lote:'Residencial urbano',
                    valor:45000000,
                    metros:105.8
                }
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
                }
            ]
        }
    },

    methods:{
        hola(){
            this.reserva = !this.reserva
            console.log(this.reserva)
        },

        simular(){
            console.log(this.meses)
            this.valor = new Intl.NumberFormat('es-ES', { style: 'currency', currency: 'COP' }).format(this.cuota)
            console.log(this.valor)
        },
    }
}
</script>

<style scope>

.sel{
    padding: 0 40px ;
}

.btn{
    font-size: 16px;
    padding: 5px 60px;
    border-radius: 50px;
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
    }

    .padding{
        padding: 25px 60px;
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
</style>