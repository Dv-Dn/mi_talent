<script>
import RolesCard from "./RolesCard";
export default {
	components: {
		RolesCard
	},
	props: {
		profiles: Array
	},
	methods: {
		calcNum(i) {
			i++;
			let tmp = i;
			let cW = document.body.clientWidth * 0.21875;
			let count;
			if (document.body.clientWidth > 270) {
				count = Math.floor(document.body.clientWidth / cW);
			}

			let row = 1;
			if (tmp > count) {
				while (tmp % count != 0) {
					tmp++;
				}
				row = tmp / count;
			}

			let rowCheck = row % 2 === 0;
			// let c = i % count;
			// if (count % 2 == 0) {
			// 	if (rowCheck) {
			// 		if (i % 2 === 0) return 0;
			// 		else return 1;
			// 	} else {
			// 		if (i % 2 === 0) return 1;
			// 		else return 0;
			// 	}
			// } else {
			// 	if (rowCheck) {
			// 		if (i % 2 === 0) return 0;
			// 		return 1;
			// 	} else {
			// 		if (i % 2 === 0) return 1;
			// 		return 0;
			// 	}
      // }
      if(rowCheck) return 1
      return 0
		}
	}
};
</script>
<template>
	<div class="roles__tab">
		<RolesCard
			:key="i + a.name"
			v-for="(a, i) in profiles"
			:name="a.name"
			:role="a.role"
			:link="a.link"
			:num="calcNum(i)"
			:photo="a.photo"
		/>
	</div>
</template>
