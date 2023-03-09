<script>
    import {createEventDispatcher} from 'svelte';
    const dispatch = createEventDispatcher();
    function handleClick(){
        dispatch('message',{
            'text':"Hello World"
        })
    }
</script>

<button on:click={handleClick}>
    Click Me.
</button>