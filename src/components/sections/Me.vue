<script setup>
import TypeWriter from '../ui/TypeWriter.vue'
</script>

<template>
	<aside>
		<div class="me-container">
			<div class="img"></div>
			<h3>Osipov Artem</h3>
			<h4><TypeWriter text="Frontend Developer" :speed="150" :delay="500" :pauseTime="2000" /></h4>
		</div>
		<hr />
		<div class="me-container">
			<div class="social-networks">
				<a href="https://github.com/Ypags">
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
						<path
							d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"
						></path>
					</svg>
				</a>
				<a href="https://t.me/prostopotato">
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
						<path
							d="M21.198 2.433a2.242 2.242 0 0 0-1.022.215l-16.5 7.5a2.25 2.25 0 0 0 .126 4.067l4.433 1.377a1.5 1.5 0 0 1 .888.888l1.377 4.433a2.25 2.25 0 0 0 4.067.126l7.5-16.5a2.25 2.25 0 0 0-1.471-2.706Z"
						></path>
						<path d="m14.5 9.5-5 5"></path>
					</svg>
				</a>
				<a href="mailto:prostoypag@yandex.ru">
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
						<rect width="20" height="16" x="2" y="4" rx="2"></rect>
						<path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"></path>
					</svg>
				</a>
				<a href="https://www.instagram.com/_prostopotato_">
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
						<rect width="20" height="20" x="2" y="2" rx="5" ry="5"></rect>
						<path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"></path>
						<line x1="17.5" y1="6.5" x2="17.51" y2="6.5"></line>
					</svg>
				</a>
			</div>
			<button>
				<i class="fa-solid fa-download"></i>
				Download CV
			</button>
		</div>
	</aside>
</template>

<style>
aside {
	background-color: var(--background-secondary);
	width: 362px;
	height: 460px;
	border-radius: 16px;
	position: fixed;
	top: 25px;
	left: 20px;
}

aside .me-container {
	display: flex;
	flex-direction: column;
	align-items: center;
}

aside .me-container .img {
	background-image: url(/img/me.jpg);
	background-repeat: no-repeat;
	background-size: cover;
	border-radius: 100%;
	width: 135px;
	height: 135px;
	border: solid 5px var(--background-primary);
	margin-top: 60px;
}

aside .me-container h3 {
	color: var(--text-primary);
	font-size: 18px;
	font-weight: 600;
	margin-top: 15px;
}

aside .me-container h4 {
	color: var(--accent-primary);
	font-size: 14px;
	font-weight: 400;
}

aside hr {
	background-color: var(--background-primary);
	height: 1px;
	width: 96%;
	margin: 35px auto 35px auto;
}

aside .me-container .social-networks {
	display: flex;
	gap: 25px;
}

aside .me-container .social-networks a {
	color: var(--text-primary);
	transition: all 0.3s ease;
}

aside .me-container .social-networks a:hover {
	color: var(--accent-primary);
	transform: translateY(-2px);
}

aside .me-container .social-networks svg {
	width: 20px;
	height: 20px;
}

aside .me-container button {
	margin-top: 30px;
	cursor: pointer;
	height: 45px;
	width: 70%;
	background-color: var(--accent-primary);
	color: var(--text-primary);
	font-size: 14px;
	font-weight: 600;
	letter-spacing: 1px;
	border: 0;
	outline: 0;
	border-radius: 40px;
	transition: all 0.4s ease;
	display: flex;
	align-items: center;
	justify-content: center;
	gap: 10px;
}

aside .me-container button i {
	font-size: 13px;
	transition: transform 0.3s ease;
}

aside .me-container button:hover {
	background-color: var(--accent-secondary);
}

aside .me-container button:hover i {
	transform: translateY(-2px);
}
</style>
