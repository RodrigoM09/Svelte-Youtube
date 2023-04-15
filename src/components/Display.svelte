<script>
    import {count} from '../stores/stores.js';

    let counter
    count.subscribe((value) => {
        counter = value;
    });
</script>

<h2>Current count is {counter}</h2>