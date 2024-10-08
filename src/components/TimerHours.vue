<template>
	<div class="timer">
		{{ horas }}:{{ minutos }}:{{ segundos }}
	</div>
</template>

<script setup>

import { reactive, computed } from "vue";

const tiempo = reactive(3600 * 3);

const horas = computed(() => {
	return tiempo % 60;
})


</script>