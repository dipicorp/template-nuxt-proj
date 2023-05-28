<script setup lang="ts">
definePageMeta({
	layout: "product-item"
})
var route = useRoute()
var productId: string = route.params.id[0]
</script>

<template>
	Product id : {{ productId }}
</template>