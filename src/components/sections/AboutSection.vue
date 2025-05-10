<script setup>
import { skills } from '@/data/skills'
</script>

<template>
	<section class="about-me" id="about-me">
		<div class="sectoin-name">
			<img src="/img/2about-me/name2.svg" alt="" />
			<span>ABOUT ME</span>
		</div>
		<h2>About <span>Me</span></h2>
		<p>
			Hi, my name is <span>Osipov Artem</span> and I am a <span>Frontend developer</span> with over 1 year of experience in designing and developing
			user-friendly and intuitive websites and features. Experience in Web development using
			<span>Vue, Nuxt.js, Typescript, TailwindCSS, JavaScript, HTML and CSS.</span>
		</p>
		<ul class="skills">
			<li v-for="skill in skills" :key="skill.name">
				{{ skill.name }}
			</li>
		</ul>
		<ul class="about-me--info">
			<li>
				<ul>
					<li>Language</li>
					<li>:</li>
					<li class="value">English, Russian</li>
				</ul>
			</li>
			<li>
				<ul>
					<li>Email</li>
					<li>:</li>
					<li class="value">prostoypag@yandex.ru</li>
				</ul>
			</li>
			<li>
				<ul>
					<li>GitHub</li>
					<li>:</li>
					<li class="value">https://github.com/Ypags</li>
				</ul>
			</li>
			<li>
				<ul>
					<li>Telegram</li>
					<li>:</li>
					<li class="value">https://t.me/prostopotato</li>
				</ul>
			</li>
		</ul>
	</section>
</template>

<style>
.about-me p span {
	font-weight: 400;
}

.about-me .skills {
	display: flex;
	gap: 10px;
	flex-wrap: wrap;
}

.about-me .skills li {
	padding: 9px 21px;
	border: dashed 2px var(--background-primary);
	border-radius: 24px;
	font-size: 14px;
	transition: all 0.2s ease;
}

.about-me .skills li:hover {
	color: var(--text-primary);
}

.about-me .about-me--info {
	margin-top: 30px;
	display: grid;
	grid-template-columns: 1fr 1fr;
}

.about-me .about-me--info ul {
	display: grid;
	grid-template-columns: 100px 30px 130px;
	font-size: 14px;
}

.about-me .about-me--info ul .value {
	color: var(--text-primary);
}
</style>
