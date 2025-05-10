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
import Me from './components/sections/ProfileSidebar.vue'
import Introduce from './components/sections/IntroduceSection.vue'
import About from './components/sections/AboutSection.vue'
import Services from './components/sections/ServicesSection.vue'
import Portfolio from './components/sections/PortfolioSection.vue'
import Education from './components/sections/EducationSection.vue'
import Nav from './components/layout/NavigationBar.vue'
import Footer from './components/layout/Footer.vue'
import ScrollToTop from './components/ui/ScrollToTop.vue'
</script>

<style></style>
