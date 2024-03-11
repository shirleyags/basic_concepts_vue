<template>
	<div>
		<button @click="ativar">Cliquei aqui!</button>
		<span v-show="ativou">Ativado</span>
	</div>
</template>

<script>
	export default {
		name: 'Reuse',
		data() {
			return {
				ativou: false
			}
		},
		methods: {
			ativar() {
				this.ativou = !this.ativou
			}
		}
	}
</script>
