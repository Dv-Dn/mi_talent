<script>
import RolesTabs from "./RolesTabs";
import RolesTab from "./RolesTab";

export default {
	components: {
		RolesTabs,
		RolesTab
	},
	data: () => ({
		current: 0,

		items: [
			{
				name: "Comedian",
				profiles: [
					{ name: "Rob Dan", role: "comedian", link: "#", photo: "4" },
					{ name: "Rob Dan", role: "comedian", link: "#", photo: "4" },
					{ name: "Rob Dan", role: "comedian", link: "#", photo: "4" },
					{ name: "Rob Dan", role: "comedian", link: "#", photo: "4" },
					{ name: "Rob Dan", role: "comedian", link: "#", photo: "4" },
					{ name: "Rob Dan", role: "comedian", link: "#", photo: "4" },
					{ name: "Rob Dan", role: "comedian", link: "#", photo: "4" },
					{ name: "Rob Dan", role: "comedian", link: "#", photo: "4" }
				]
			},
			{
				name: "Actor",
				profiles: [
					{ name: "Rob Dan", role: "Actor", link: "#", photo: "2" },
					{ name: "Rob Dan", role: "Actor", link: "#", photo: "2" },
					{ name: "Rob Dan", role: "Actor", link: "#", photo: "2" },
					{ name: "Rob Dan", role: "Actor", link: "#", photo: "3" },
					{ name: "Rob Dan", role: "Actor", link: "#", photo: "2" },
					{ name: "Rob Dan", role: "Actor", link: "#", photo: "2" },
					{ name: "Rob Dan", role: "Actor", link: "#", photo: "2" },
					{ name: "Rob Dan", role: "Actor", link: "#", photo: "qq" }
				]
			}
		]
	})
};
</script>
<template>
	<section class="roles container">
		<RolesTabs :current="current" :items="items" @click="i => (current = i)" />
		<RolesTab :profiles="items[current].profiles" />
	</section>
</template>
