<template>
	<section class="my-education" id="my-education">
		<div class="sectoin-name">
			<img src="/img/5my-education/name5.svg" alt="" />
			<span>RESUME</span>
		</div>
		<h2>My <span>Education</span></h2>
		<div class="my-education--container">
			<div class="block">
				<h6>Novosibirsk Chemical-Technological College named after D. I. Mendeleyev</h6>
				<h5>2023-2027</h5>
			</div>
			<span></span>
			<hr />
			<div>
				<h4>Information systems and programming</h4>
				<p>Secondary vocational education</p>
			</div>
		</div>
	</section>
</template>

<style>
.my-education .my-education--container {
	margin-top: 40px;
	display: flex;
	gap: 50px;
	position: relative;
}

.my-education .my-education--container h6 {
	font-size: 16px;
	font-weight: 500;
	color: var(--text-primary);
	width: 190px;
}

.my-education .my-education--container .block h5 {
	font-weight: 400;
	font-size: 14px;
}

.my-education .my-education--container hr {
	background-color: var(--text-secondary);
	width: 1px;
	height: 120px;
}

.my-education .my-education--container span {
	background-color: var(--accent-primary);
	width: 10px;
	height: 10px;
	border-radius: 50%;
	box-shadow: 0px 0px 6px var(--text-secondary);
	position: absolute;
	left: 235px;
}

.my-education .my-education--container h4 {
	font-size: 23px;
	font-weight: 500;
	color: var(--text-primary);
}

footer {
	text-align: center;
	padding: 24px 0;
	font-size: 14px;
}
</style>
