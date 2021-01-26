<script>
  import Logo from './Logo.svelte';
  import MenuIcon from './MenuIcon.svelte';

  let showMenu = false
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
    position: relative;
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

  @media screen and (max-width: 475px) {
    header {
      height: 72px;
      position: fixed;
      top: 0;
      background-color: white;
      z-index: 50;
      width: 100%;
      border-bottom: none;
      box-shadow: 0px 3px 3px rgba(0, 0, 0, 0.07), 0px 3px 4px rgba(0, 0, 0, 0.06), 0px 1px 8px rgba(0, 0, 0, 0.1);
    }

		.left {
      width: 100%;
      justify-content: space-between;
    }

    .right {
      position: absolute;
      top: 72px;
      width: auto;
      height: auto;
      right: 0;
      padding: 10px;
      display: inline-flex;
      flex-direction: column;
      align-items: flex-end;
      z-index: 999;
      background-color: white;
      border-radius: 6px;
      transform: translate3d(150px, 0, 0);
      opacity: 0;
      box-shadow: 0px 6px 10px rgba(0, 0, 0, 0.14), 0px 1px 18px rgba(0, 0, 0, 0.12), 0px 3px 5px rgba(0, 0, 0, 0.2);
      transition: .2s ease all;
    }

    .right.show {
      opacity: 1;
      transform: translate3d(0, 0, 0);
    }

    .right a {
      margin-bottom: 12px;
      display: block;
      padding: 10px;
    }

    .right a:hover:after {
      height: auto;
    }

    .mobile-overlay {
      background-color:rgba(0, 0, 0, 0.2);
      position: fixed;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
      z-index: 998;
    }
	}
  
</style>

<header>
	<div class='left'>
    <Logo />
    {#if (showMenu)}
      <div on:click={() => showMenu = false} class='mobile-overlay' />
    {/if}
    <MenuIcon isActive={showMenu} onClick={() => showMenu = !showMenu} />
	</div>

  <nav class='right' class:show={showMenu}>
    <a href='#hangers' on:click={() => showMenu = false}>Hangers</a>
    <a href='#about' on:click={() => showMenu = false}>About</a>
    <a href='#contact' on:click={() => showMenu = false}>Contact</a>
    <a href='https://www.etsy.com/shop/perpetualhang' on:click={() => showMenu = false} target='blank'>Shop on Etsy &rarr;</a>
  </nav>

</header>