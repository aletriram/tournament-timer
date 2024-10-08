<template>
	<div class="timer">
		<div id="tiempo">
			{{ horas }}:{{ minutos }}:{{ segundos }}
		</div>
		<button type="button" class="btn btn-primary" @click="toggleStart">Start</button>
	</div>
</template>

<script setup>

import { reactive, computed } from "vue";

const tiempo = reactive(3600 * 3);

const horas = computed(() => {
	return Math.floor((tiempo / 60) / 60);
});

const minutos = computed(() => {
	return (tiempo / 60) % 60;
});

const segundos = computed(() => {
	return tiempo % 60;
});

</script>