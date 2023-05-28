<script setup lang="ts">
// interface Props {
// 	title?: string
// }
// defineProps<Props>()
</script>

<template>
	<button @click="e => $emit('some-event', e)" class="bg-green-600 rounded-full px-2 py-1 active:opacity-90 text-white">
		<slot />
	</button>
</template>