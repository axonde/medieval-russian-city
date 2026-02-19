<script>
	import Image from '$lib/Image.svelte';
	import Scene from '$lib/Scene.svelte';
	import Background from '$lib/Background.svelte';
	import Timeline from '$lib/Timeline.svelte';
	import Copyright from '$lib/Copyright.svelte';
	import Preview from '$lib/Preview.svelte';

	let scenes = $state();
</script>

<Background />

<div class="wrapper">
	<!-- {#if scenes} -->
	<!-- 	<Timeline values={[1220, 1240, 1241, 1242, 1251, 1257, 1263]} bind:bind={scenes} /> -->
	<!-- {/if} -->

	<div class="scenes" bind:this={scenes}>
		<Preview title="Средневековый русский город" text="VI–XVII вв." />

		<Scene
			title="Типы &ensp;&ensp;&ensp;&ensp;&ensp; поселений"
			text="Город, пригород, посад, слобода, погост, село, деревня, починок. Город – укреплённый административный и военный центр."
		>
			{#snippet img()}
				<Image url="art-1.png" />
			{/snippet}
		</Scene>

		<Scene
			alternate={true}
			title="Кремль, &ensp;&ensp;&ensp;&ensp;&ensp; посад &ensp;&ensp;&ensp;&ensp;&ensp; и &ensp;&ensp;&ensp;&ensp;&ensp; слободы"
			text="Кремль (град) – крепость с собором и администрацией. Посад – торгово-ремесленная часть. Слободы – привилегированные поселения за стенами."
		>
			{#snippet img()}
				<Image url="art-2.png" />
			{/snippet}
		</Scene>

		<Scene
			title="Оборонительные <br> сооружения"
			text="Деревянные и каменные стены с башнями, рвы, валы, остроги, засеки. На южных рубежах – укреплённые линии с надолбами."
		>
			{#snippet img()}
				<Image url="art-3.png" />
			{/snippet}
		</Scene>

		<Scene
			alternate={true}
			title="Улицы &ensp;&ensp;&ensp;&ensp;&ensp; и &ensp;&ensp;&ensp;&ensp;&ensp; жилые &ensp;&ensp;&ensp;&ensp;&ensp; постройки"
			text="Улицы немощёные, в грязь клали деревянные мостки. Дома деревянные, рубленые «во мху», у богатых – хоромы с теремами и резьбой."
		>
			{#snippet img()}
				<Image url="art-4.png" />
			{/snippet}
		</Scene>

		<Scene
			title="Церкви &ensp;&ensp;&ensp;&ensp;&ensp; и <br> административные <br> постройки"
			text="Церкви (часто каменные), приказная изба, воеводский двор, гостиный двор, тюрьма, житницы, пороховые погреба."
		>
			{#snippet img()}
				<Image url="art-5.png" />
			{/snippet}
		</Scene>

		<Scene
			alternate={true}
			title="Органы &ensp;&ensp;&ensp;&ensp;&ensp; власти"
			text="Воевода (назначался царём), приказная изба с дьяками. На посаде – земская изба, выборные старосты и целовальники."
		>
			{#snippet img()}
				<Image url="art-6.png" />
			{/snippet}
		</Scene>

        <Scene
			alternate={false}
			title="Москва &ensp;&ensp;&ensp;&ensp;&ensp; X&ensp;&ensp;V&ensp;&ensp;I&ensp;&ensp;&ensp;&ensp;&ensp;–&ensp;&ensp;&ensp;&ensp;&ensp;X&ensp;&ensp;V&ensp;&ensp;I&ensp;&ensp;I &ensp;&ensp;&ensp;&ensp;&ensp; веков"
			text="Кремль, Китай-город, Белый город, Земляной город, слободы. Огромный по тем временам мегаполис с 40 тысячами домов."
		>
			{#snippet img()}
				<Image url="art-7.png" />
			{/snippet}
		</Scene>

        <Scene
			alternate={true}
			title="Повседневная &ensp;&ensp;&ensp;&ensp;&ensp; жизнь"
			text="Ремёсла, торговля, служба. Патриархальный уклад, религиозность. Рынки, лавки, ремесленные мастерские."
		>
			{#snippet img()}
				<Image url="art-8.png" />
			{/snippet}
		</Scene>

        <Scene
			alternate={false}
			title="Значение &ensp;&ensp;&ensp;&ensp;&ensp; древнерусских <br> городов"
			text="Центры политической, экономической и культурной жизни. Основа обороны и объединения русских земель."
		>
			{#snippet img()}
				<Image url="art-9.png" />
			{/snippet}
		</Scene>


		<Copyright />
	</div>
</div>

<style>
	.wrapper {
		display: flex;
		gap: 40px;
		width: 100%;
	}
	.scenes {
		display: flex;
		flex-direction: column;
		flex-grow: 1;
		user-select: none;
		-webkit-user-select: none;
		-moz-user-select: none;
		overflow-y: scroll;
		height: 100vh;
		/* padding-left: 300px; */
		scroll-snap-type: y mandatory;
		align-items: center;
	}
</style>
