<script>
export default {
	props: {
		items: Array,
		current: Number
	}
};
</script>

<template>
	<ul class="roles__tabs-list">
		<li
			:key="index + item.name"
			v-for="(item, index) in items"
			:class="[
				'roles__tabs-item',
				{ 'roles__tabs-item_active': index === current }
			]"
			@click="$emit('click', index)"
		>
			{{ item.name }}
		</li>
	</ul>
</template>
