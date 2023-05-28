<script setup lang="ts">
var count = ref(0)
var countDisplay = computed<string>(() => {
	if (count.value > 10) {
		return "Greater than 10"
	}
	return `${count.value}`
})

function increase() {
	count.value++
}
</script>


<template>
	<main class="p-2 flex flex-col">
		See more <a href="https://vuejs.org/api/reactivity-core.html">https://vuejs.org/api/reactivity-core.html</a>
		<div class="border border-gray-300 rounded-md p-2 mb-2">
			<div>Formal:</div>
			<div>{{ countDisplay }}</div>
			<button @click="increase">Increase</button>
		</div>
		<div class="border border-gray-300 rounded-md p-2 flex flex-col items-start">
			<div>Quick:</div>
			<div>{{ count > 10 ? "greater than 10" : count }}</div>
			<button v-on:click="count++">Increase</button>
			<Button @some-event="count++" class="mt-2" title="Increase it!"></Button>
		</div>
	</main>
</template>