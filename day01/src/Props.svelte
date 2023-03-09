<script>
    /***
     * 当在App.svelte中调用组件并传递参数时
     * answer的默认值不会生效
     * 只有当在App.svelte中没有传递answer参数时
     * answer的默认值才会生效
    */
    export let answer = 'Svelte';
</script>
<style>
    p {
		color: orangered;
		font-family: 'Comic Sans MS', cursive;
		font-size: 2em;
	}
</style>
<p>The answer is {answer}.</p>

