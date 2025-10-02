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
		<Preview title="Промышленность России" text="в XVII векe" />

		<Scene
			title="Первые &ensp;&ensp;&ensp;&ensp;&ensp; мануфактуры"
			text="Зарождение крупного производства в эпоху после Смуты. Ответ на вызовы времени: необходимость сильной армии и экономики. Закладка фундамента для будущих петровских реформ."
		>
			{#snippet img()}
				<Image url="art-1.png" />
			{/snippet}
		</Scene>

		<Scene
			alternate={true}
			title="Нужна &ensp;&ensp;&ensp;&ensp;&ensp; современная <br> армия &ensp;&ensp;&ensp;&ensp;&ensp; и &ensp;&ensp;&ensp;&ensp;&ensp; экономика"
			text="Слабость ремесленного производства после Смутного времени. Острая потребность государства в оружии, металле, униформе. Необходимость импортозамещения военных поставок. Поиск новых форм организации труда."
		>
			{#snippet img()}
				<Image url="art-2.png" />
			{/snippet}
		</Scene>

		<Scene
			title="Государственный &ensp;&ensp;&ensp;&ensp;&ensp; заказ <br> и &ensp;&ensp;&ensp;&ensp;&ensp; разделение &ensp;&ensp;&ensp;&ensp;&ensp; труда"
			text="Главная особенность — ведущая роль государства как заказчика и организатора. Принцип разделения труда для повышения эффективности. Работа на казну, а не на рынок. Использование как вольного, так и принудительного труда."
		>
			{#snippet img()}
				<Image url="art-3.png" />
			{/snippet}
		</Scene>

		<Scene
			alternate={true}
			title="Виды &ensp;&ensp;&ensp;&ensp;&ensp; мануфактур"
			text="Казенные — государственные (Оружейная палата). Купеческие — частные (солеварни Строгановых). Посессионные — с приписанными к заводу государственными крестьянами. Уникальная русская модель, основанная на крепостном праве."
		>
			{#snippet img()}
				<Image url="art-4.png" />
			{/snippet}
		</Scene>

		<Scene
			title="Причины &ensp;&ensp;&ensp;&ensp;&ensp; роста"
			text="Война, экспансия, государственный интерес. Внешние угрозы (войны с Речью Посполитой, Швецией). Освоение новых территорий (Урал, Сибирь). Политика меркантилизма — стремление к экономической независимости. Государство как главный 'менеджер' промышленного развития"
		>
			{#snippet img()}
				<Image url="art-5.png" />
			{/snippet}
		</Scene>

		<Scene
			alternate={true}
			title="Заложен &ensp;&ensp;&ensp;&ensp;&ensp; фундамент <br> российской &ensp;&ensp;&ensp;&ensp;&ensp; промышленности"
			text="Создана основа для тяжелой и военной промышленности. Освоен Урал — будущая 'металлургическая кладовая' России. Сформирована модель государственно-зависимой промышленности. Прямой путь к масштабным реформам Петра I."
		>
			{#snippet img()}
				<Image url="art-6.png" />
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
