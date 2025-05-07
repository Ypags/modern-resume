<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isVisible = ref(false)

const checkScroll = () => {
	isVisible.value = window.scrollY > 300
}

const scrollToTop = () => {
	window.scrollTo({
		top: 0,
		behavior: 'smooth',
	})
}

onMounted(() => {
	window.addEventListener('scroll', checkScroll)
})

onUnmounted(() => {
	window.removeEventListener('scroll', checkScroll)
})
</script>

<template>
	<Transition name="fade">
		<button v-if="isVisible" @click="scrollToTop" class="scroll-to-top" aria-label="Scroll to top">
			<svg
				xmlns="http://www.w3.org/2000/svg"
				width="24"
				height="24"
				viewBox="0 0 24 24"
				fill="none"
				stroke="currentColor"
				stroke-width="2"
				stroke-linecap="round"
				stroke-linejoin="round"
			>
				<path d="M12 19V5M5 12l7-7 7 7" />
			</svg>
		</button>
	</Transition>
</template>

<style scoped>
.scroll-to-top {
	position: fixed;
	bottom: 30px;
	right: 30px;
	width: 50px;
	height: 50px;
	border-radius: 50%;
	background: var(--accent-primary);
	border: none;
	color: var(--text-primary);
	cursor: pointer;
	display: flex;
	align-items: center;
	justify-content: center;
	transition: all 0.3s ease;
	box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
}

.scroll-to-top:hover {
	background: var(--accent-secondary);
	transform: translateY(-5px);
	box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
}

/* Анимации появления и исчезновения */
.fade-enter-active,
.fade-leave-active {
	transition: all 0.3s ease;
}

.fade-enter-from,
.fade-leave-to {
	opacity: 0;
	transform: translateY(20px);
}

@media (max-width: 768px) {
	.scroll-to-top {
		bottom: 20px;
		right: 20px;
		width: 40px;
		height: 40px;
	}
}
</style>
