<script>
	import Header from './Header.svelte';
	import Footer from './Footer.svelte';
	import ClickablePhoto from './ClickablePhoto.svelte';
	import About from './About.svelte';
	import Contact from './Contact.svelte';
	
	export let name;

</script>

<svelte:head>
	<style>
		:root {
			--primary-dark: #051F20;
			--primary-text: #1A413A;
			--secondary-text: #0B2B26;
			--text-light: #DAF1DE;
		}
	</style>
</svelte:head>


<Header />
<main>
	<div id='hangers' class='images-wrapper'>
		<div class='carousel'>
			<ClickablePhoto
				name='Northern Lights Black Spruce Hang - Raw green aventurine anchor, malachi...'
				imgSrc='https://www.dl.dropboxusercontent.com/s/zb9ymnw7i6hzsq0/il_1588xN.2837273481_q2z0.jpg?dl=0'
				linkTo='https://www.etsy.com/in-en/listing/941228405/northern-lights-black-spruce-hang?ref=shop_home_active_2'
			/>
			<ClickablePhoto
				name='Magic Earth Hang - Quartz Crystal Anchor, Unakite & Goldstone Beads'
				imgSrc='https://www.dl.dropboxusercontent.com/s/61dyu0ngcxsor7m/il_1588xN.2708210111_g1hp.jpg?dl=0'
				linkTo='https://www.etsy.com/in-en/listing/904501921/magic-earth-hang-macrame-plant-hanger?ref=shop_home_active_4'
			/>
			<ClickablePhoto
				name='Two Tier Golden Hang - Amethyst & rose quartz beads with tinsel tassel'
				imgSrc='https://i.etsystatic.com/21824466/r/il/cbfd60/2390402037/il_1588xN.2390402037_8b0b.jpg'
				linkTo='https://www.etsy.com/in-en/listing/818720467/two-tier-golden-hanger-long-with?ref=shop_home_active_18'
			/>
			<div class='h-spacer' />
		</div>
	</div>
	<About />
	<div class='info-wrapper'>
		<Contact />
	</div>
</main>
<Footer />

<style>
	main {
		text-align: center;
		padding: 0;
		margin: 0 auto;
	}

	.info-wrapper {
		padding: 0 25px;
	}

	.images-wrapper {
		height: calc(90vh - 100px);
	}

	.carousel {
		box-sizing: border-box;
		position: relative;
		display: flex;
		padding: 24px 15px;
		height: 100%;
		overflow: scroll;
	}

	.carousel::-webkit-scrollbar {
		width: 0px;  /* Remove scrollbar space */
		background: transparent;  /* Optional: just make scrollbar invisible */
	}

	.h-spacer {
		width: 1px;
		flex-shrink: 0;
	}

	@media screen and (max-width: 475px) {
		main {
			padding-top: 72px;
		}

		.images-wrapper {
			height: calc(100vh - 72px);
		}

		.info-wrapper {
			padding: 15px;
		}
	}
</style>