<template>
	<nav class="d-flex justify-content-between py-3" id="main-navbar">
		<div class="d-flex "> 
			<div class="d-inline-block">
				<img src="../assets/images/logo.png" id="main-logo">
			</div>
			<div class="d-inline-block px-4">
				<ul class="p-0 d-flex no-ul-list-style " id="navbar-main-menu">
					<li><a href="#">Dashboard</a></li>
					<li><a href="#">Messages</a></li>
					<li><a href="#">Orders</a></li>
					<li><a href="#">Gigs</a></li>
					<li><a href="#">Analytics</a></li>
					<li><a href="#">Earnings</a></li>
				</ul>
			</div>
		</div>
		<div class="d-flex justify-content-end ">
			<div class="dropdown d-inline-block position-relative" >
				<img src="../../public/images/avatar.png" class="avatar-img" >
				<div class="d-none shadow rounded mt-2 dropdown-menu">
					<ul class="no-ul-list-style py-4 px-0 m-0 d-flex justify-content-start">
						<li class="d-block"><a href="#">Main Menu</a></li>
						<li class="d-block"><a href="#">Messages</a></li>
						<li class="d-block"><a href="#">Orders</a></li>
						<li class="d-block"><a href="#">Gigs</a></li>
						<li class="d-block"><a href="#">Logout</a></li>
					</ul>
				</div>
			</div>
			
		</div>
	</nav>
</template>
<style scoped>
	.container{
		width: 100%;
		max-width: 1200px;
		margin: 0px auto;
	}
</style>