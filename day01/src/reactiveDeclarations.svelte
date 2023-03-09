<script>
    let count = 0;
    // 使用$:在Svelte中启用响应式声明
    $: double = count * 2;
    // 使用$:在Svelte中启用响应式语句
    $: if(count==0){
        console.error(`This value is too low for count,got ${count}`)
    } else {
        console.log(`We got a good pretty good value for count,which is ${count}`)
    }
</script>

<!-- <p>
    {count} doubled is {double};
</p> -->