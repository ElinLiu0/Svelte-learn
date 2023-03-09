<script>
	import Forward from "./Forward.svelte"
	function handleClick(event){
		alert(event.detail.text);
	}
</script>

<Forward on:message={handleClick}/>