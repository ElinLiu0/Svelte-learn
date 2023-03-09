<script>
    let numbers = [1,2,3,4];

    function insert(){
        /**
         * 由于Svelte中的响应式语句有且仅能被赋值型语句触发
         * 因此我们可以使用扩展运算符:...将原有的number展开后，并在末尾添加最新值
         * 值得一提的是：此处我们不是对原始的数组进行扩容，实际上是创建了一个新的数组
         * 并覆盖了原始的numbers
        */
        numbers = [...numbers, numbers.length + 1];
    }
    /**
     * 使用Array.prototype.reduce()对其进行扩容，
     * 其中第一个参数为待执行的回调函数：接受两个参数t和n，并将t+n的结果回调
     * 该回调过程遍历整个数组
     */
    $: sum = numbers.reduce((t, n) => t + n, 0);
</script>

<p>
    {numbers.join(' + ')} = {sum}
</p>
<button on:click={insert}>
	Add a number
</button>