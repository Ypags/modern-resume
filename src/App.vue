<template>
	<div class="wrapper">
		<div class="container">
			<main>
				<Me />
				<Introduce />
				<About />
				<Services />
				<Portfolio />
				<Education />
				<Footer />
			</main>
			<Nav />
		</div>
		<ScrollToTop />
	</div>
</template>

<script setup>
import Me from './components/sections/Me.vue'
import Introduce from './components/sections/Introduce.vue'
import About from './components/sections/About.vue'
import Services from './components/sections/Services.vue'
import Portfolio from './components/sections/Portfolio.vue'
import Education from './components/sections/Education.vue'
import Nav from './components/layout/Nav.vue'
import Footer from './components/layout/Footer.vue'
import ScrollToTop from './components/ui/ScrollToTop.vue'
</script>

<style></style>
