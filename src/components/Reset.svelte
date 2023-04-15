<script>
    import {count} from '../stores/stores.js';

    // update() is a function that takes a callback function as an argument
    function Reset() {
        count.set(0);
    }
</script>

<button on:click={Reset}>Reset</button>