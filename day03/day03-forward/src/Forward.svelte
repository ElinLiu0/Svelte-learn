<script>
    import Dispatch from "./Dispatch.svelte";
    import {createEventDispatcher} from 'svelte';
    const dispatch = createEventDispatcher();
    function forward(event){
        dispatch("message",event.detail)
    }
</script>

<Dispatch on:message={forward}/>