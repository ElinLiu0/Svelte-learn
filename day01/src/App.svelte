<script>
	import Nested from './Nested.svelte';
	import Image from './Image.svelte'
	// 使用import关键字从现有的.svelte文件中导入组件
	import DirectRender from "./DirectRender.svelte";
	import ReactiveDeclarations from "./reactiveDeclarations.svelte";
	import LogicalExpression from "./LogicalExpression.svelte";
	let count = 0;
	function adder(){
		count += 1;
	}
	import ReactiveInArrays from "./reactiveInArrays.svelte";
	import Props from "./Props.svelte";
	import Info from './Info.svelte';
	const info = {
		name: '柳轶霖',
		age: '22',
		sex: '男',
		hobby: '写代码'
	}
</script>
<style>
	/* p {
		color: orangered;
		font-family: 'Comic Sans MS', cursive;
		font-size: 2em;
	} */
</style>

<!-- <p>Hello Svelte.</p> -->
<!-- <Nested/>
<Image/> -->
<!-- <DirectRender/> -->
<!--使用on:click执行在script标签中或.js文件中定义好的function()-->
<!-- <button on:click={adder}>点击了{count}次</button> -->
<!-- <ReactiveDeclarations/> -->
<!-- <ReactiveInArrays/> -->
<!-- <Props answer={42}/> -->
<!--通过展开运算符将object完整传递到组件中-->
<Info {...info}/>
