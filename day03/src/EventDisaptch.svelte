<script>
    // 从svelte组件库中引入事件指派器
    import {createEventDispatcher} from 'svelte';
    // 实例化
    const dispatch = createEventDispatcher();
    function handleClick(){
        /**
         * 使用指派器将信息进行指派，指派的类型为message
         * 指派的数据位对象，包含一个值为"Hello World"的键，键名为text
        */
        dispatch('message',{
            'text':'Hello World'
        })
    }
</script>

<button on:click={handleClick}>
    Click Me!
</button>