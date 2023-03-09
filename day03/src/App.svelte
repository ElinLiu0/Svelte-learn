<script>
	import Await from "./Await.svelte";
	import Event from "./Event.svelte";
	import EventLimit from "./EventLimit.svelte";
	import EventDisaptch from "./EventDisaptch.svelte";
	function handleMessage(event){
		alert(event.detail.text)
	}
</script>

<!-- <Await/> -->
<!-- <Event/> -->
<!-- <EventLimit/> -->
<EventDisaptch on:message={handleMessage}/>