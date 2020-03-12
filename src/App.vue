<script>
// import Header from "@/components/Header";
import Header from "@/components/Header";
import Roles from "@/components/Roles";

export default {
	name: "App",
	components: { Header, Roles },
	methods: {}
};
</script>

<template>
	<div id="app">
		<Header />
		<Roles />
	</div>
</template>

<style lang="scss">
@import "@/scss/main";
</style>
