<template>
	<div class="event-page">
		<NuxtContent :document="event" />
	</div>
</template>

<script>
export default {
	async asyncData({ $content, params }) {
		const event = await $content(`events/${params.slug}`, 'index').fetch()
		return { event }
	},
	name: "EventPage"
}
</script>
