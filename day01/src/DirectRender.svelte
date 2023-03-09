<script>
    let string = "<strong>Hello World</strong>";
    let markdown = "```python print(1) ```";
</script>
<!--使用@html 直接将string中的html内容进行渲染-->
<p>{@html string}</p>