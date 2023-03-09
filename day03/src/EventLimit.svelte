<script>
    function handleClick(){
        alert("只显示一次！")
    }
</script>
<!--使用类似once,capture这类的关键字以限制事件的执行-->
<button on:click|once={handleClick}>
    点我
</button>