<template>
	<section class="introduce" id="introduce">
		<div class="sectoin-name">
			<img src="/img/1introduce/name1.svg" alt="" />
			<span>INTRODUCE</span>
		</div>
		<h2>Building Fluid<br /><span>User Experiences</span></h2>
		<p>I'm a <span>Web3 Frontend developer</span> at heart, writing efficient and highly adaptive code suitable for tasks of any level.</p>
		<ul>
			<li><img src="/img/1introduce/marker.svg" alt="" />Available for work</li>
			<li><img src="/img/1introduce/marker.svg" alt="" />Full Time Job</li>
		</ul>
	</section>
</template>

<style>
main {
	width: 61%;
	margin-left: 410px;
}

section {
	background-color: var(--background-secondary);
	border-radius: 16px;
	padding: 50px;
	margin-top: 25px;
}

section .sectoin-name {
	display: flex;
	align-items: center;
	gap: 8px;
	padding: 9px 21px;
	border: solid 2px var(--background-primary);
	border-radius: 40px;
	width: 130px;
}

section .sectoin-name span {
	color: var(--text-primary);
	font-size: 12px;
}

section h2 {
	margin-top: 31px;
	color: var(--text-primary);
	font-size: 48px;
	font-weight: 200;
	line-height: 61px;
}

section h2 span {
	color: var(--accent-primary);
	font-weight: 600;
}

section p {
	margin: 24px 0;
	width: 78%;
}

section p span {
	color: var(--text-primary);
	font-weight: 700;
}

.introduce ul {
	display: flex;
	gap: 40px;
}

.introduce ul li {
	display: flex;
}
</style>
