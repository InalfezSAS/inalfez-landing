<template >
  <div class="modal-mision">
		<div class="contenedor-mision ">
			<header class="d-flex justify-content-end mb-4">
				<label for="modal-mision" class="btn btn-primary">X</label>
			</header>
			<div class="contenido-mision">
				<h1>Misión</h1>
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
#modal-mision{
	display: none;
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
	background: rgba(0,0,0,0.5);
	transition: all 500ms ease;
	opacity: 0;
	visibility: hidden;
}

.contenedor-mision{
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

.contenido-mision{
	width: 100%;
}

.contenido-mision h1 {
    font-weight: 700;
    font-size: 25px;
		margin-bottom: 20px;
}

.contenido-mision p {
    font-size: 18px;
}

#modal-mision:checked ~ .modal-mision{
	opacity: 1;
	visibility: visible;
}

#modal-mision:checked ~ .modal-mision .contenedor-mision{
	transform: translateY(0%);
}

@media (max-width:768px){
	.contenedor-mision{
		width: 95%;
		height: 95%;
	}
}
</style>