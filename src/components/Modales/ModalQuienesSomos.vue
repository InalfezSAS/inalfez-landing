<template >
  <div class="modal">
		<div class="contenedor ">
			<header class="d-flex justify-content-end mb-4">
				<label for="modal-quienes" class="btn btn-primary">X</label>
			</header>
			<div class="contenido">
				<h1>¿Quiénes Somos?</h1>
				<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Illum nesciunt inventore praesentium id maiores quasi aut recusandae quibusdam accusantium quia cum, numquam repellendus labore amet nemo nobis dolor quae voluptatibus?</p>
			</div>
		</div>
	</div>
</template>
<script>
export default {
  
}
</script>
<style >
#modal-quienes{
	display: none;
}

.modal {
	width: 100%;
	height: 100vh;
	display: flex;
	justify-content: center;
	align-items: center;
	position: fixed;
	top: 0;
	left: 0;
	background: rgba(0,0,0,0.5);
	transition: all 500ms ease;
	opacity: 0;
	visibility: hidden;
}

.contenedor{
	width: 600px;
	height: 400px;
	padding: 20px;
	margin: auto;
	border-radius: 20px;
	background: #fff;
	box-shadow: 1px 7px 25px rgba(0,0,0,0.6);
	transition: all 500ms ease;
	position: relative;
	transform: translateY(-30%);
}

.contenido{
	width: 100%;
}

.contenido h1 {
    font-weight: 700;
    font-size: 25px;
		margin-bottom: 20px;
}

.contenido p {
    font-size: 18px;
}

#modal-quienes:checked ~ .modal{
	opacity: 1;
	visibility: visible;
}

#modal-quienes:checked ~ .modal .contenedor{
	transform: translateY(0%);
}

@media only screen and (min-width:320px) and (max-width:768px){
	.contenedor{
		width: 95%;
	}
}
</style>