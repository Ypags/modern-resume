<template>
	<section class="my-services" id="my-services">
		<div class="sectoin-name">
			<img src="/img/3my-services/name3.svg" alt="" />
			<span>SERVICES</span>
		</div>
		<h2>My <span>Services</span></h2>
		<div class="blocks">
			<div class="block">
				<div>01</div>
				<img src="/img/3my-services/block1.svg" alt="" />
				<h3>UI/UX Design</h3>
				<h4>I help designers with improving UI/UX for better performance and quality</h4>
			</div>
			<div class="block">
				<div>02</div>
				<img src="/img/3my-services/block2.svg" alt="" />
				<h3>Web Development</h3>
				<h4>Building frontend applications from design, developing backend and designing database</h4>
			</div>
		</div>
	</section>
</template>

<style>
.my-services .blocks {
	display: flex;
	margin-top: 40px;
	justify-content: space-between;
}

.my-services .block {
	width: 48%;
	position: relative;
	border: solid 1px var(--background-primary);
	border-radius: 16px;
	padding: 15px 25px 40px;
}

.my-services .block div {
	text-align: center;
	font-size: 72px;
	font-weight: 700;
	color: var(--background-secondary);
	-webkit-text-stroke: 1px var(--text-secondary);
	transition: all 0.3s ease;
}

.my-services .block img {
	position: absolute;
	right: 30px;
	top: 40px;
	transition: all 0.3s ease;
}

.my-services .block:hover div {
	-webkit-text-stroke: 1px var(--text-primary);
}

.my-services .block:hover img {
	rotate: -45deg;
}

.my-services .block h3 {
	color: var(--text-primary);
	font-size: 24px;
	font-weight: 500;
	margin-bottom: 15px;
}

.my-services .block h4 {
	font-size: 16px;
	font-weight: 400;
}
</style>
