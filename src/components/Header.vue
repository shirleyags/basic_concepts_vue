<template>
	<ul>
		<li><a href="#">Home</a></li>
		<li><a href="#">Projetos</a></li>
		<li><a href="#">Contato</a></li>
	</ul>
    
</template>

<script>
	export default {
		name:'Header'
	}
	</script>

	<!-- Exemplo de CSS local -->
	<style scoped>
		ul {
			list-style: none;
			display: flex;
			background: #999;
		}
		li {
			margin-right: 10px;
		}
		a {
			color: #DDD;
			text-decoration: none;
			transition: .5s;
		}
		a:hover {
			color: #40E0D0;
		}
</style>
