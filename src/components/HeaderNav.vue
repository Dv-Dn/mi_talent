<script>
import Search from "./UI/Search";
export default {
	components: {
		Search
	}
};
</script>

<template>
	<div class="header-nav padding">
		<!-- nav -->
		<nav class="nav">
			<svg
				xmlns="http://www.w3.org/2000/svg"
				height="24"
				viewBox="0 0 24 24"
				width="24"
			>
				<path d="M0 0h24v24H0z" fill="none" />
				<path d="M3 18h18v-2H3v2zm0-5h18v-2H3v2zm0-7v2h18V6H3z" />
			</svg>
			<ul class="nav__ul">
				<li class="nav__li"><a href="#">clients</a></li>
				<li class="nav__li"><a href="#">news</a></li>
			</ul>
			<!-- <img src="@/assets/icons/bars.svg" alt="" /> -->
		</nav>
		<!-- logo -->
		<div class="header-logo">
			<img src="@/assets/Logo.png" alt="" class="header-logo__img" />
		</div>
		<!-- search -->
		<Search />
		<!-- <svg
			xmlns="http://www.w3.org/2000/svg"
			height="24"
			viewBox="0 0 24 24"
			width="24"
		>
			<path
				d="M15.5 14h-.79l-.28-.27C15.41 12.59 16 11.11 16 9.5 16 5.91 13.09 3 9.5 3S3 5.91 3 9.5 5.91 16 9.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z"
			/>
			<path d="M0 0h24v24H0z" fill="none" />
		</svg> -->
	</div>
</template>
