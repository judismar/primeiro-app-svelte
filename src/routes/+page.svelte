<script lang='ts'>
	let cont: number = $state(0);
	abstract class Incrementador
	{
		public static incrementa(): void
		{
			cont ++;
		}
	}
</script>

<button onclick={Incrementador.incrementa}>
	Clicou {cont} vezes.
</button>

{#if cont > 10}
	<p>Você REALMENTE gosta MUITO de clicar!</p>
{:else if cont < 5}
	<p>Nada a declarar.</p>
{:else}
	<p>Você gosta de clicar!</p>
{/if}
