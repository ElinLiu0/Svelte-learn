<script>
    let a = 10;
</script>

{#if a > 10}
	<p>{a} is greater than 10</p>
{:else if 5 > a}
	<p>{a} is less than 5</p>
{:else}
	<p>{a} is between 5 and 10</p>
{/if}