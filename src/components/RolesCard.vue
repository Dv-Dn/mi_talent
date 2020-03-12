<script>
export default {
	props: {
		name: String,
		role: String,
		photo: String,
		link: String,
		num: [Number, String]
	}
};
</script>
<template>
	<div
		class="roles-card"
		:data-num="num"
		:style="{
			'background-image': 'url(' + require('@/assets/photo/' + photo + '.png')
		}"
	>
		<!-- Link or to(router) -->
		<a :href="link">
			<div class="roles-card__hover">
				<div class="roles-card__icon-block">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 31.49 31.49"
						class="roles-card__icon"
					>
						<path
							d="M21.205,5.007c-0.429-0.444-1.143-0.444-1.587,0c-0.429,0.429-0.429,1.143,0,1.571l8.047,8.047H1.111
	C0.492,14.626,0,15.118,0,15.737c0,0.619,0.492,1.127,1.111,1.127h26.554l-8.047,8.032c-0.429,0.444-0.429,1.159,0,1.587
	c0.444,0.444,1.159,0.444,1.587,0l9.952-9.952c0.444-0.429,0.444-1.143,0-1.571L21.205,5.007z"
						/>
					</svg>
				</div>
				<article class="roles-card__info-block">
					<h3 class="roles-card__name">{{ name }}</h3>
					<p class="roles-card__role">{{ role }}</p>
				</article>
			</div>
		</a>
	</div>
</template>
