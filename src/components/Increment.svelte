<script>
    import {count} from '../stores/stores.js';

    // update() is a function that takes a callback function as an argument
    function Increment() {
        count.update(n => n + 1);
    }
</script>

<button on:click={Increment}>Increment</button>