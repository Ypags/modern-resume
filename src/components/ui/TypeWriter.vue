<script setup>
import { ref, onMounted, watch } from 'vue'

const props = defineProps({
	text: {
		type: String,
		required: true,
	},
	speed: {
		type: Number,
		default: 100,
	},
	delay: {
		type: Number,
		default: 0,
	},
	pauseTime: {
		type: Number,
		default: 2000,
	},
})

const displayText = ref('')
const isTyping = ref(false)
const isDeleting = ref(false)

const typeText = async () => {
	while (true) {
		// Печатаем текст
		isTyping.value = true
		isDeleting.value = false
		displayText.value = ''

		// Добавляем задержку перед началом печати
		await new Promise(resolve => setTimeout(resolve, props.delay))

		// Печатаем вперед
		for (let i = 0; i < props.text.length; i++) {
			displayText.value += props.text[i]
			await new Promise(resolve => setTimeout(resolve, props.speed))
		}

		// Пауза после печати
		await new Promise(resolve => setTimeout(resolve, props.pauseTime))

		// Печатаем назад
		isDeleting.value = true
		for (let i = props.text.length; i > 0; i--) {
			displayText.value = props.text.substring(0, i - 1)
			await new Promise(resolve => setTimeout(resolve, props.speed / 2))
		}

		// Пауза после удаления
		await new Promise(resolve => setTimeout(resolve, props.pauseTime / 2))
	}
}

// Начинаем печать при монтировании компонента
onMounted(() => {
	typeText()
})

// Следим за изменением текста
watch(
	() => props.text,
	() => {
		typeText()
	}
)
</script>

<template>
	<span class="typewriter"> {{ displayText }}<span class="cursor" :class="{ typing: isTyping, deleting: isDeleting }">|</span> </span>
</template>

<style scoped>
.typewriter {
	display: inline-block;
}

.cursor {
	display: inline-block;
	margin-left: 2px;
	animation: blink 1.5s step-end infinite;
}

.cursor.typing {
	animation: none;
}

.cursor.deleting {
	animation: blink 0.5s step-end infinite;
}

@keyframes blink {
	0%,
	100% {
		opacity: 1;
	}
	50% {
		opacity: 0;
	}
}
</style>
