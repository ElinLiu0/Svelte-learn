<script>
	let data = { x: 0, y: 0 };
	// 创建一个函数用户获取输入事件
	function handleMousemove(event) {
		// 令data中的x和y为终端鼠标指针的x和y坐标
		data.x = event.clientX;
		data.y = event.clientY;
	}
</script>

<style>
	div { width: 100%; height: 100%; }
</style>

<div on:mousemove={handleMousemove}>
	当前鼠标光标在：{data.x} x {data.y}。
</div>