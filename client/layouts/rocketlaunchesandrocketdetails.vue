<template >
	<v-app class="hero">
		<v-main>
			<div>
				<header>
					<nav>
						<v-app-bar class="custom-nav bg-grey-lighten-1">
							<ul class="d-flex ">
							<li><NuxtLink class="custom-nav" to="/">Home</NuxtLink></li>
							<li><NuxtLink class="custom-nav" to="/rocketLaunches">Rocket Launches</NuxtLink></li>
							<li><NuxtLink class="custom-nav" to="/rocketDetails">Rocket Details</NuxtLink></li>
        		</ul>
						</v-app-bar>
						
					</nav>
				</header>
			</div>

      <slot />
		</v-main>
	</v-app>
</template>

<style scoped>
	
	.hero {
    background: url('https://wallpaperaccess.com/full/1268171.jpg') no-repeat center center fixed;
  	background-size: cover;
  }

	.custom-nav {
		border-bottom-left-radius: 5px;
		border-bottom-right-radius: 5px;
		text-decoration: none;
		color: #333333;
	}

	li {
		list-style: none;
		margin: 0px 20px;
	}

</style>

<script>

</script>
