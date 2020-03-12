<script>
export default {
	props: {
		current: Number,
		list: Array
	},
	data: () => ({
		isopen: false
	}),
	methods: {
		numberToString(i) {
			i++;
			if (i < 10) {
				return "0" + i;
			}
			return i;
		}
	}
};
</script>
<template>
	<div :class="['header-profile-list', { 'header-profile-list_open': isopen }]">
		<div class="header-profile-list__block">
			<ul class="header-profile-list__list">
				<li
					:key="index"
					v-for="(item, index) in list"
					:class="[
						'header-profile-list__item',
						{ 'header-profile-list__item_active': current == index }
					]"
					@click="
						() => {
							$emit('click', index);
							isopen = false;
						}
					"
				>
					<span class="header-profile-list__number">{{
						numberToString(index)
					}}</span>
					<hr class="header-profile-list__hr" />
				</li>
			</ul>
		</div>
		<svg
			xmlns="http://www.w3.org/2000/svg"
			x="0px"
			y="0px"
			viewBox="0 0 512.13 512.13"
			width="24"
			class="header-profile-list__icon"
			@click="isopen = !isopen"
		>
			<g>
				<g>
					<path
						d="M256.065,0C114.43,0,0,114.298,0,256.065S114.298,512.13,256.065,512.13S512.13,397.832,512.13,256.065
			S397.702,0,256.065,0z M256.065,477.892c-122.891,0-221.828-98.937-221.828-221.828S133.175,34.236,256.065,34.236
			s221.828,98.937,221.828,221.828S378.956,477.892,256.065,477.892z"
					/>
				</g>
			</g>
			<g>
				<g>
					<path
						d="M199.827,254.373l98.937-98.937c6.769-6.9,6.769-17.184,0-23.953c-6.769-6.769-17.054-6.769-23.953,0L163.897,242.397
			c-3.385,3.385-5.077,6.769-5.077,11.977c0,5.077,1.692,8.591,5.077,11.977l112.606,112.606c3.385,3.385,6.769,5.077,11.977,5.077
			c3.385,0,8.592-1.692,10.284-6.769c6.769-6.769,6.769-17.053,0-23.953L199.827,254.373z"
					/>
				</g>
			</g>
		</svg>
	</div>
</template>
