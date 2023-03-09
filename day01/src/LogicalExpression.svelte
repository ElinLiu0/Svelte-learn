<script>
    let count = 0;
    function adder(){
        count += 1;
    }
</script>


<button on:click={adder}>
    Your clicked {count} {count === 1 ? 'time':'times'}
</button>