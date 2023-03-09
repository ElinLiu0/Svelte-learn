<script>
    let promise = getResp();
    // 定义异步请求函数
    async function getResp() {
        // 使用fetchAPI请求URL
        const res = await fetch("https://jsonplaceholder.typicode.com/todos/1",{method:'GET'})
        // 异步等待响应JSON
        const text = await res.text()
        // 如果响应的状态为OK
        if(res.ok){
            // 则返回text
            return text
        } else {
            // 反之抛出异常
            throw new Error(text);
        }
    }
    function handleClick() {
        promise = getResp();
    }
</script>

<button on:click={handleClick}>
    Click me
</button>
<!--使用await块异步等待promise中的数据-->
{#await promise}
    <p>...waiting</p>
<!--当异步等待获得到正确的响应时，则显示该段数据-->
{:then data}
    <p style="color:green">{data}</p>
<!--如果在异步等待的过程中发生异常则显示错误信息-->
{:catch error}
    <p style="color:darkred">{error.message}</p>
{/await}