<script>
    const names = [
        {
            firsName: 'Bruce',
            lastName: 'Wayne'
        },
        {
            firsName: 'Clark',
            lastName: 'Kent'
        },
        {
            firsName: 'Diana',
            lastName: 'Prince'
        }
    ]
</script>
{#each names as name(name)}
    <h3>{name.firsName} {name.lastName}</h3>
{/each}