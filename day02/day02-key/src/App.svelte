<script>
	import KeyOfEach from "./KeyOfEach.svelte";
	let things = [
		{ id: 1, color: '#0d0887' },
		{ id: 2, color: '#6a00a8' },
		{ id: 3, color: '#b12a90' },
		{ id: 4, color: '#e16462' },
		{ id: 5, color: '#fca636' }
	];
	function toggle(){
		// 减少一个元素
		things = things.slice(1)
	}
</script>

<button on:click={toggle}>
	Remove First
</button>

{#each things as thing}
	<!--将16进制颜色码作为参数传递给组件-->
	<KeyOfEach current={thing.color}/>
{/each}