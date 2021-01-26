<script>
  import Logo from './Logo.svelte';
</script>

<style>
  a {
		color: var(--secondary-text);
    text-decoration: none;
    height: 100%;
    display: flex;
    align-items: center;
    font-size: 18px;
    font-weight: 300;
    padding: 0 10px;
    position: relative;
  }

  a:after {
    height: 0;
    content: '';
    width: 100%;
    background-color: var(--secondary-text);
    position: absolute;
    bottom: 0;
    left: 0;
    transition: .2s ease all;
  }
  
  a:hover {
    color: var(--secondary-text);
  }

  a:hover:after {
    height: 5px;
  }

  header {
    box-sizing: border-box;
		height: 100px;
		display: flex;
		align-items: center;
		justify-content: space-between;
		border-bottom: 1px solid var(--secondary-text);
		padding: 0 25px;
	}

	.left {
		height: 70%;
		margin-top: 4px;
		display: flex;
    align-items: center;
  }
  
  .right {
    height: 100%;
    width: 400px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
</style>

<header>
	<div class='left'>
		<Logo />
	</div>


  <nav class='right'>
    <a href='#hangers'>Hangers</a>
    <a href='#about'>About</a>
    <a href='#contact'>Contact</a>
    <a href='https://www.etsy.com/shop/perpetualhang' target='blank'>Shop on Etsy &rarr;</a>
  </nav>

</header>