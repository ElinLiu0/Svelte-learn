<script>
    let data = [
        {"message":"a"},
        {"message":"b"}
    ]
</script>

<ul>
    <!--使用each展开js中的对象数组（json）-->
    <!--each块支持两个参数（key），第一个是待遍历元素的数据-->
    <!--第二个是索引值-->
    {#each data as cat,i}
    <li>
        This cat {i+1} names {cat.message}.
    </li>
    {/each}
</ul>