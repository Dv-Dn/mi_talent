<script>
import HeaderNav from "./HeaderNav";
import HeaderProfile from "./HeaderProfile";
import HeaderProfileList from "./HeaderProfileList";

export default {
	components: {
		HeaderNav,
		HeaderProfile,
		HeaderProfileList
	},
	data: () => ({
		current: 0,
		profiles: [
			{
				name: "Robert Downey ",
				role: "American actor",
				photo: "robda",
				links: {
					facebook: "#",
					instagram: "#",
					youtube: "#",
					twitter: "#"
				}
			},
			{
				name: "Derek Qs",
				role: "British Comedian",
				photo: "4",
				links: {
					facebook: "#",
					instagram: "#",
					youtube: "#",
					twitter: "#"
				}
			},
			{
				name: "Derek Qs",
				role: "British Comedian",
				photo: "3",
				links: {
					facebook: "#",
					instagram: "#",
					youtube: "#",
					twitter: "#"
				}
			},
			{
				name: "Derek Qs",
				role: "British Comedian",
				photo: "qq",
				links: {
					facebook: "#",
					instagram: "#",
					youtube: "#",
					twitter: "#"
				}
			}
		]
	}),
	methods: {
		switchProfile(i) {
			this.current = i;
		},
		numberToString(i) {
			i++;
			if (i < 10) {
				return "0" + i;
			}
			return i;
		},
		changeProfile(i) {
			this.current = i;
		}
	}
};
</script>

<template>
	<header class="header container">
		<div class="header__square"></div>
		<HeaderNav />
		<section class="header__profile-block">
			<HeaderProfile
				:name="profiles[current].name"
				:role="profiles[current].role"
				:photo="profiles[current].photo"
				:links="profiles[current].links"
				:number="numberToString(current)"
			/>
			<HeaderProfileList
				:list="profiles"
				:current="current"
				@click="changeProfile"
			/>
			<!-- <div class="header-right"></div> -->
		</section>
	</header>
</template>
