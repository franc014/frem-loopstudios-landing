<ul
	class="flex flex-col full-width gap items-center justify-center text-sm"
	style="--gap-size: 1rem; "
>
	<li><a href="#">About</a></li>
	<li><a href="#">Careers</a></li>
	<li><a href="#">Events</a></li>
	<li><a href="#">Product</a></li>
	<li><a href="#">Support</a></li>
</ul>

<style>
	ul li a {
		color: hsl(var(--crl-white));
		text-decoration: none;
		display: block;
	}

	@media screen and (min-width: 850px) {
		ul {
			flex-direction: row;
			justify-content: flex-start;
			align-items: flex-start;
		}

		ul li {
			padding: 0;
		}

		ul li a:hover::after {
			content: '';
			display: block;
			height: 1px;
			background-color: hsl(var(--crl-white));
			width: 60%;
			margin-inline: auto;
		}
	}
</style>
