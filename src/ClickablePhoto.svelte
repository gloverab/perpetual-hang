<script>
  export let imgSrc
	export let linkTo = '/'
	export let name

  let showOverlay = false
</script>

<style>
  a.image-wrapper {
		position:relative;
		flex: 1;
		height: 100%;
		color: #DAF1DE;
		border-radius: 6px;
		margin-right: 24px;
		box-shadow: 0px 3px 3px rgba(0, 0, 0, 0.14), 0px 3px 4px rgba(0, 0, 0, 0.12), 0px 1px 8px rgba(0, 0, 0, 0.2);
	}

	img {
		width: auto;
		height: 100%;
		border-radius: inherit;
	}

	.overlay {
		box-sizing: border-box;
		position: absolute;
		display: flex;
		align-items: flex-end;
		justify-content: flex-end;
		width: 100%;
		bottom: 0;
		left: 0;
		height: 25%;
		border-radius: inherit;
		opacity: 0;
		padding: 24px;
    transition: .2s ease all;
		background: rgba(0,0,0,.8);
		background: -moz-linear-gradient(0deg, rgba(0,0,0,0.8183648459383753) 0%, rgba(3,3,3,0.773546918767507) 45%, rgba(0,0,0,0) 100%);
		background: -webkit-linear-gradient(0deg, rgba(0,0,0,0.8183648459383753) 0%, rgba(3,3,3,0.773546918767507) 45%, rgba(0,0,0,0) 100%);
		background: linear-gradient(0deg, rgba(0,0,0,0.8183648459383753) 0%, rgba(3,3,3,0.773546918767507) 45%, rgba(0,0,0,0) 100%);
		filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#000000",endColorstr="#000000",GradientType=1);
	}

	.overlay-text {
		text-align: left;
		font-size: 24px;
		font-weight: 500;
		margin: 0;
		width: calc(70% - 24px);
		margin-right: 24px;
	}

	.cta-span {
		padding: 15px 20px;
		border-radius: 12px;
		background-color: white;
		color: var(--primary-dark);
		font-size: 16px;
		width: 30%;
		min-width: 120px;
	}
	
	a:hover {
		box-shadow: 0px 6px 10px rgba(0, 0, 0, 0.14), 0px 1px 18px rgba(0, 0, 0, 0.12), 0px 3px 5px rgba(0, 0, 0, 0.2);
	}
  
  a:hover .overlay {
    opacity: 1;
	}
	
	@media screen and (max-width: 475px) {
		a.image-wrapper {
			box-sizing: border-box;
			width: 100%;
			overflow: hidden;
			flex-shrink: 0;
			flex: none;
		}

		.overlay {
			opacity: 1;
		}

		.overlay-text {
			display: none;
			font-size: 18px;
			width: 100%;
		}

		.cta-span {
			/* width: 120px; */
		}
	}
</style>

<a href={linkTo} class='image-wrapper img-1' target='blank'>
  <img src={imgSrc} alt='Macrame Plant Hanger' />
  <div class='overlay'>
		<h3 class='overlay-text'>{name}</h3>
		<span class='cta-span'>
			Buy me today!
		</span>
    
  </div>
</a>