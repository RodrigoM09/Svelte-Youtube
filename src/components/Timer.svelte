<script>
    import { time, elapsedTime } from '../stores/stores.js';

    const dateFormatter = new Intl.DateTimeFormat('en-US', {
        hour: 'numeric',
        minute: '2-digit',
        second: '2-digit',
        hour12: true
    });
</script>

<h2>The time is {dateFormatter.format($time)}</h2>
<h2>Elapsed time {$elapsedTime}</h2>