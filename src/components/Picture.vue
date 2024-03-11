<template>
	<img :src="avatar" :alt="descricao">
	<ChangeImage @change-image="changeOtherImage"/>
</template>

<script>
	import ChangeImage from './ChangeImage.vue'
	export default {
		name: 'Picture',
		components: { 
			ChangeImage 
		},
		data() {
			return {
				avatar: "/img/avatar.png",
				descricao: "Shirley Alice"
			}
		},
		methods: {
			changeOtherImage() {
				this.avatar = "/img/avatar2.png"
			}
		}
	}
</script>
