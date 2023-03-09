<script>
	let word;
	let x;
	let y;
	let yes = false;
	function handleClick(){
		console.log(!yes)
	}
	let scoops = 1;
	let flavours = ["薄荷巧克力"];
	let menu = [
		"奶油曲奇",
		"薄荷巧克力",
		"树莓味"
	]
	function join(flavours){
		if(flavours.length==1){
			return flavours[0]
		}
		return `${flavours.slice(0, -1).join(', ')} and ${flavours[flavours.length - 1]}`;
	}
</script>

<input type="text" bind:value={word}>



<div class="container">
	<div class="sub">
		{#if word==undefined}
		<p>请输入些文字：</p>
		{:else}
			<p>Hello {word}</p>
		{/if}
	</div>
	<div class="sub">
		<input type=number bind:value={x} min=0 max="10">
		<input type=range bind:value={x} min="0" max="10">
		<br>
		<input type=number bind:value={y} min=0 max="10">
		<input type=range bind:value={y} min="0" max="10">
		<p>{x}+{y}={x+y}</p>
	</div>
	<div class="sub">
		<input type="checkbox" bind:checked={yes} on:click={handleClick}>遵守上述条款以加入我们
		{#if yes}
		<p>感谢支持！</p>
		{:else}
		<p>请同意条款！</p>
		{/if}
		<button disabled={!yes}>
			Go!
		</button>
	</div>
	<div class="sub">
		<h2>计量</h2>
		{#each [1,2,3] as scop}
			<label for="">
				<input type="radio" bind:group={scoops} value={scop}>
				{scop}
			</label>
		{/each}
		<h2>口味</h2>
		{#each menu as flavour}
			<label for="">
				<input type="checkbox" bind:group={flavours} value={flavour}>
				{flavour}
			</label>
		{/each}
		{#if flavours.length==0}
			<p>请选择至少一种口味哦！</p>
		{:else if flavours.length > scoops}
			<p>无法预订超过计量的口味！</p>
		{:else}
			<p>
				您预定了{scoops}个冰淇淋，口味分别为：{join(flavours)}。
			</p>
		{/if}
	</div>
</div>

