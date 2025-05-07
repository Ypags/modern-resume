<script setup>
import { ref, onMounted } from 'vue'

const isDark = ref(true)

const toggleTheme = () => {
	isDark.value = !isDark.value
	document.documentElement.classList.toggle('light')
}

onMounted(() => {
	// Проверяем сохраненную тему
	const savedTheme = localStorage.getItem('theme')
	if (savedTheme === 'light') {
		isDark.value = false
		document.documentElement.classList.add('light')
	}
})

// Сохраняем тему при изменении
const handleThemeChange = () => {
	toggleTheme()
	localStorage.setItem('theme', isDark.value ? 'dark' : 'light')
}
</script>

<template>
	<button @click="handleThemeChange" class="theme-toggle" :class="{ 'is-dark': isDark }" aria-label="Toggle theme">
		<div class="toggle-track">
			<div class="toggle-thumb">
				<svg
					v-if="isDark"
					class="moon"
					xmlns="http://www.w3.org/2000/svg"
					viewBox="0 0 24 24"
					fill="none"
					stroke="currentColor"
					stroke-width="2"
					stroke-linecap="round"
					stroke-linejoin="round"
				>
					<path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"></path>
				</svg>
				<svg
					v-else
					class="sun"
					xmlns="http://www.w3.org/2000/svg"
					viewBox="0 0 24 24"
					fill="none"
					stroke="currentColor"
					stroke-width="2"
					stroke-linecap="round"
					stroke-linejoin="round"
				>
					<circle cx="12" cy="12" r="5"></circle>
					<line x1="12" y1="1" x2="12" y2="3"></line>
					<line x1="12" y1="21" x2="12" y2="23"></line>
					<line x1="4.22" y1="4.22" x2="5.64" y2="5.64"></line>
					<line x1="18.36" y1="18.36" x2="19.78" y2="19.78"></line>
					<line x1="1" y1="12" x2="3" y2="12"></line>
					<line x1="21" y1="12" x2="23" y2="12"></line>
					<line x1="4.22" y1="19.78" x2="5.64" y2="18.36"></line>
					<line x1="18.36" y1="5.64" x2="19.78" y2="4.22"></line>
				</svg>
			</div>
		</div>
	</button>
</template>

<style scoped>
.theme-toggle {
	background: none;
	border: none;
	padding: 0;
	cursor: pointer;
	margin-top: 10px;
}

.toggle-track {
	width: 40px;
	height: 22px;
	background-color: var(--background-primary);
	border: 2px solid var(--background-primary);
	border-radius: 30px;
	position: relative;
	transition: all 0.3s ease;
}

.toggle-thumb {
	width: 18px;
	height: 18px;
	background-color: var(--accent-primary);
	border-radius: 50%;
	position: absolute;
	top: 0;
	left: 0;
	transition: all 0.3s ease;
	display: flex;
	align-items: center;
	justify-content: center;
}

.theme-toggle.is-dark .toggle-thumb {
	transform: translateX(18px);
}

.theme-toggle svg {
	width: 12px;
	height: 12px;
	color: var(--text-primary);
	transition: all 0.3s ease;
}

.theme-toggle .moon {
	transform: rotate(0deg);
}

.theme-toggle .sun {
	transform: rotate(0deg);
}

.theme-toggle:hover .toggle-thumb {
	background-color: var(--accent-secondary);
}

.theme-toggle:hover .moon {
	transform: rotate(15deg);
}

.theme-toggle:hover .sun {
	transform: rotate(15deg);
}
</style>
