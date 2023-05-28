<script setup lang="ts">
var ids: number[] = [1, 2, 3, 4, 5, 6]
</script>


<template>
	<main class="p-2">
		<h1 class="text-2xl pb-3">
			All products page
		</h1>
		<div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 gap-2">
			<template v-for="id in ids" :key="id">
				<a :href="'/products/' + id" class="bg-pink-200 p-2 rounded-md">
					<div class="text-xl font-light pb-3 text-gray-700">
						Product id: {{ id }}
					</div>
					<div>Click to see detail</div>
				</a>
			</template>
		</div>

	</main>
</template>