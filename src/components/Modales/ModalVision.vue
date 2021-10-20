<template >
  <div class="modal-vision">
		<div class="contenedor-vision ">
			<header class="d-flex justify-content-end mb-4">
				<label for="modal-vision" class="btn btn-primary">X</label>
			</header>
			<div class="contenido-vision">
				<h1>Visión</h1>
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
#modal-vision{
	display: none;
}

.modal-vision {
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

.contenedor-vision{
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

.contenido-vision{
	width: 100%;
}

.contenido-vision h1 {
    font-weight: 700;
    font-size: 25px;
		margin-bottom: 20px;
}

.contenido-vision p {
    font-size: 18px;
}

#modal-vision:checked ~ .modal-vision{
	opacity: 1;
	visibility: visible;
}

#modal-vision:checked ~ .modal-vision .contenedor-vision{
	transform: translateY(0%);
}

@media (max-width:768px){
	.contenedor-vision{
		width: 95%;
		height: 95%;
	}
}
</style>