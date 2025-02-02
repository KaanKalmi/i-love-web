<script>
</script>

<header>
	<div class="header-content">
		<h1>Kaan K.</h1>
		<ul>
			<li>
				<a href="https://www.linkedin.com/in/kaan-kalmioglu/" target="_blank" class="header-link">
					<i class="fab fa-linkedin"></i>
					<em>Visit my Linkedin</em>
				</a>
			</li>
			<li>
				<a href="mailto:kalmioglu.k@gmail.com" class="header-link">
					<i class="fas fa-envelope"></i>
					<em>Mail me</em>
				</a>
			</li>
		</ul>
	</div>
</header>

<style>
	header {
		padding: 2rem 0 1rem 0;
		color: var(--primary-color);
		text-align: center;
  	font-size: 2rem;
	}

	.header-content {
		display: flex;
		justify-content: left;
		align-items: flex-start;
		flex-direction: column;

		& ul{
			list-style-type: none;
			padding: 0;
			margin: 0;

			& li{
				display: inline;
				margin: 0 20px 0 0;

				& .header-link {
					color: var(--primary-color); 
					font-size: 1.5rem;
					text-decoration: none;

					& i {
						color: var(--icon-color);
					}

					& em {
						font-size: 1rem;
						color: var(--text-color);
					}
			}
		}
    }
	}
	.header-link:hover {
    color: var(--btn-bg);
  }  

  .header-link:hover i {
    color: var(--btn-bg);
  }
</style>
