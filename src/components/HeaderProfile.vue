<script>
import HeaderButton from "./HeaderButton";
export default {
	props: {
		name: String,
		role: String,
		photo: String,
		number: String,
		links: Object
	},
	components: {
		HeaderButton
	}
};
</script>

<template>
	<div class="header-profile">
		<div
			class="header-profile__bg"
			:style="{
				'background-image': 'url(' + require('@/assets/photo/' + photo + '.png')
			}"
		>
		</div>
		<ul class="header-profile__links padding">
			<li
				:key="key + '_' + link"
				v-for="(link, key) in links"
				class="header-profile__link"
			>
				<a :href="link">
					<img
						:src="require('@/assets/icons/' + key + '.svg')"
						:alt="key"
						class="header-profile__img"
				/></a>
			</li>
		</ul>
		<div class="header-profile__main">
			<div class="header-profile__number-block padding">
				<hr class="header-profile__hr" />
				<span class="header-profile__number">{{ number }}</span>
			</div>
			<article class="header-profile__info">
				<h1 class="header-profile__name">{{ name }}</h1>
				<p class="header-profile__role">{{ role }}</p>
			</article>
		</div>
		<HeaderButton />
	</div>
</template>
