<template>
	<div class="scol-page">
		<NuxtContent :document="scol" />
	</div>
</template>

<script>
export default {
	async asyncData({ $content, params }) {
		const scol = await $content(`scol${params.year}/${params.slug}`, 'index').fetch()
		return { scol }
	},
	name: "ScolPage"
}
</script>
