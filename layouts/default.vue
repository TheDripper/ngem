<template>
  <div>
<nav class="navbar cont" role="navigation" aria-label="main navigation">
  <div class="navbar-brand">
    <a class="navbar-item" href="https://bulma.io">
      <img src="/logo.png" width="248" height="49" id=logo>
    </a>
    <a role="button" class="navbar-burger burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
    </a>
  </div>
  <div id="navbarBasicExample" class="navbar-menu">
    <div class="navbar-start">
    </div>
    <div class="navbar-end">
    <a class="navbar-item">Home</a>
    <a class="navbar-item">Contact</a>
    <a class="navbar-item">Client Login</a>
    <div class="navbar-item">
    	<form id=search action="/search">
		<div class="field">
		  <div class="control">
		    <input class="input" type="text" placeholder="search...">
		  </div>
		</div>
	</form>
    </div>
    </div>
  </div>
</nav>
    

    <nuxt/>
  </div>
</template>
<style>
.cont {
	width: 100%;
	max-width: 1140px;
	margin: 0 auto;
}
#logo {
	max-height: none;
}
</style>
