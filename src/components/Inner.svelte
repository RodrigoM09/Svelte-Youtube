<script>
    import {createEventDispatcher} from 'svelte';
    const dispatch = createEventDispatcher();

    function greet() {
        dispatch('greet', 'hello')
        }
</script>
<button on:click={greet}>Greet</button>