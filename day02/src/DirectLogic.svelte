<script>
    let user = {loggedIn: false};
    function toggle(){
        // 取当前值的反值
        user.loggedIn = !user.loggedIn;
    }
</script>

<!--在界面端进行隐式逻辑处理-->
{#if user.loggedIn}
    <button on:click={toggle}>
        登出
    </button>
{:else}
    <button on:click={toggle}>
        登录
    </button>
{/if}