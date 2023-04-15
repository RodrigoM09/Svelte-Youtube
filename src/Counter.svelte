<script>
    let count = 0;
    
    function clickHandler() {
        count += 1;
    }
</script>

<h2>Count - {count}</h2>
<button on:click={clickHandler}>Increment</button>