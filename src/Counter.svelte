<script>
	export let initialCounter = 0;
  export let maxCounter = 9;

	let contador = initialCounter

	function handleClick () {
		contador++
	}

  $: isEvenOrOdd = contador % 2 === 0 ? 'Is Even' : 'Is Odd'
  $: if (contador > maxCounter) {
    contador = maxCounter
  }
</script>

<main>
	<button on:click={handleClick}>Incrementar</button>
	<span>{contador}</span>
	<span class="suave">{isEvenOrOdd}</span>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 440px;
		margin: 0 auto;
	}

	span {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}
	.suave {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 2rem;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>