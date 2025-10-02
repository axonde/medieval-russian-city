<script>
	let { title, text, img, alternate = null } = $props();
</script>

<div class="content__wrapper">
	<div class="content__container {alternate ? 'alternate' : ''}">
		<div class="content">
			<div class="content__text--wrapper">
				<div
					class="title bg-gradient-to-b from-white to-neutral-400 bg-clip-text text-3xl text-transparent"
				>
					{@html title}
				</div>
				<div class="text">{text}</div>
			</div>
		</div>
		<div class="img__wrapper">
			{@render img()}
		</div>
	</div>
</div>

<style>
	.content__wrapper {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
		padding: 0px 35px 30px 0;
		scroll-snap-align: center;
		flex-shrink: 0;
	}
	.content__container {
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.content__container.alternate {
		flex-direction: row-reverse;
	}
	.content {
		display: flex;
		justify-content: flex-end;
		min-width: 50%;
	}
	.content__container.alternate .content {
		justify-content: flex-start;
	}
	.content__text--wrapper {
		display: flex;
		gap: 50px;
		flex-direction: column;
		position: relative;
		z-index: 2;
		flex-shrink: 0;
		width: max-content;
	}
	.title {
		padding: 10px 20px 10px 0;
		letter-spacing: -17px;
		font: var(--font-main);
		font-size: 48px;
		white-space: normal;
		text-wrap: nowrap;
	}
	.text {
		max-width: 440px;
		padding: 0 15px;
		font: var(--font-text);
		font-size: 30px;
	}
	.text:after {
		content: '';
		background: url('/pattern.jpg');
		background-size: 40%;
		height: 30px;
		border-radius: 10px;
		width: 100%;
		display: block;
		margin-top: 15px;
	}
	.img__wrapper {
		align-self: self-end;
		max-width: 45%;
		max-height: calc(0.7 * 100vh);
		position: relative;
		z-index: 1;
		padding: 40px;
	}
</style>
