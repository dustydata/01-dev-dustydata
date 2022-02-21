<!-- src/routes/__layout.svelte -->
<nav id="nav">
	<ul id="ul">
		<li>
		<a href="/">Home</a>
		</li>
		<li>
		<a href="/about">About</a>
		</li>
		<li>
			<a href="/login">Login</a>
		</li>
		<li>	
			<a href="/settings">Settings</a>
		</li>
	</ul>

</nav>

<style>
	nav {
		background-color: #EEEEEE;
		margin: 10;
        padding: 10;
        width: 200px;
	}
	ul {
	list-style-type: none;
    color: #000000;
    font-weight:bold;
    padding: 8px 16px;
    text-decoration: none;
	}
	li a {
		display: block;
		padding: 8px;
		background-color: #dddddd;
		width: 60;
	}


</style>

 <slot></slot> 
 