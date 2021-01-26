<script lang='ts'>
  export let
    isActive,
    fill,
    onClick

  function handleClick () {
    onClick()
	}
</script>

<style>
  .menu-icon {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: flex-end;
    width: 28px;
    height: 14px;
    cursor: pointer;
    z-index: 999;
    transition: .2s ease all;

  }
  .menu-line {
    background-color: var(--primary-dark);
    height: 3px;
    border-radius: 3px;
    transition: .3s ease all;
  }
  .menu-line-1 {
    width: 100%;
  }

  .menu-line-2 {
    width: 75%;
  }

  .isActive .menu-line.menu-line-1 {
    transform: translateY(180%) rotate(45deg);
  }

  .isActive .menu-line.menu-line-2 {
    width: 100%;
    transform: translateY(-180%) rotate(135deg);
  }


  @media only screen and (min-width: 475px) {
    .menu-icon {
      display: none;
    }
  }
</style>

<div class="menu-icon" class:isActive id='menu-icon' on:click={handleClick}>
  <div class='menu-line menu-line-1'></div>
  <div class='menu-line menu-line-2'></div>
</div>