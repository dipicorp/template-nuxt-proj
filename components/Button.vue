<script setup lang="ts">
interface Props {
	title?: string
}
var props = defineProps<Props>()
</script>

<template>
	<button @click="e => $emit('some-event', e)" class="bg-green-600 rounded-full px-2 py-1 active:opacity-90 text-white">
		<!-- {{ title == null ? <slot /> : title }}		 -->
		<template v-if="props.title == null">
			<slot></slot>
		</template>
		<template v-else>
			{{ props.title }}
		</template>
	</button>
</template>