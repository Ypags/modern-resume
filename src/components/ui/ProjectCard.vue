<script setup>
defineProps({
	title: {
		type: String,
		required: true,
	},
	category: {
		type: String,
		required: true,
	},
	image: {
		type: String,
		required: true,
	},
})
</script>

<template>
	<div class="block">
		<h4>{{ title }}</h4>
		<span>{{ category }}</span>
		<div class="block-img"><img :src="image" :alt="title" /></div>
	</div>
</template>

<style>
.my-projects .block {
	width: 49%;
	height: 27%;
	border: solid 1px var(--background-primary);
	margin-bottom: 2%;
	border-radius: 12px;
	position: relative;
}

.my-projects .block h4 {
	position: absolute;
	top: 50%;
	left: 50%;
	transform: translate(-50%, -50%);
	color: #fff;
	font-size: 20px;
	opacity: 0;
	z-index: 100;
	transition: all 0.5s ease;
	scale: 1.15;
}

.my-projects .block span {
	position: absolute;
	top: 16%;
	left: 81%;
	transform: translate(-50%, -50%);
	color: var(--text-primary);
	opacity: 0;
	z-index: 100;
	font-size: 14px;
	transition: all 0.3s ease;
	padding: 5px 16px;
	background-color: var(--background-primary);
	border-radius: 17px;
}

.my-projects .block-img {
	height: 100%;
	padding: 13px;
}

.my-projects .block-img img {
	border-radius: 12px;
	width: 100%;
	height: 100%;
	object-fit: cover;
}

.my-projects .block:hover .block-img {
	filter: blur(1.7px);
}

.my-projects .block:hover span {
	opacity: 1;
}

.my-projects .block span:hover {
	cursor: pointer;
	color: var(--accent-primary);
}

.my-projects .block:hover h4 {
	opacity: 1;
	scale: 1;
}

.my-projects .block::before {
	transition: all 0.5s ease;
	content: '';
	width: 100%;
	height: 100%;
	position: absolute;
	z-index: 10;
	background: linear-gradient(0deg, rgba(0, 0, 0, 0.9) 0%, rgba(255, 255, 255, 0) 100%);
	border-radius: 12px;
	opacity: 0;
}

.my-projects .block:hover::before {
	opacity: 1;
}
</style>
