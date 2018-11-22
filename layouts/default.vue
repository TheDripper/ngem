<template>
<div id=ngem>
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

<nav class="foot cont">
    <span id="footer-span-l">Copyright 2011-2018, Northgate Environmental Management, Inc. All Rights Reserved.</span>
    <a id="thumbtack" href="http://www.thumbtackstudios.com" title="Thumbtack Studios|homepage">Web and Graphic Design | Berkeley | Thumbtack Studios</a>
</nav>



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
@font-face {
	font-family: "steiner";
	src: url("/steiner.ttf");
}
h1 {
	font-family: "steiner";
	font-size: 36px;
}
h2 {
	font-family: "steiner";
	font-size: 24px;
}
.foot {
	background: #eee;
	border-radius: 5px;
	padding: 10px;
	display: flex;
	justify-content: space-between;

}
#ngem {
	//width: 100vw;
	//height: 100vh;
	//display: flex;
	//flex-direction: column;
	//justify-content: flex-start;
	//align-items: center;
}
</style>
