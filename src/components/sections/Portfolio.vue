<script setup>
import Project from '../ui/project.vue'
import { projects } from '../../data/projects'
</script>

<template>
	<section class="my-projects" id="my-projects">
		<div class="sectoin-name">
			<img src="/img/4my-projects/name4.svg" alt="" />
			<span>PORTFOLIO</span>
		</div>
		<h2>My <span>Projects</span></h2>
		<div class="blocks">
			<Project v-for="(project, index) in projects" :key="index" :title="project.title" :category="project.category" :image="project.image" />
		</div>
	</section>
</template>

<style>
.my-projects .blocks {
	margin-top: 40px;
	display: flex;
	flex-wrap: wrap;
	justify-content: space-between;
}
</style>
