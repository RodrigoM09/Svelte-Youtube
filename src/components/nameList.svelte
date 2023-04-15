<script>
    const names = [
        {
            firstName: 'Bruce',
            lastName: 'Wayne'
        },
        {
            firstName: 'Clark',
            lastName: 'Kent'
        },
        {
            firstName: 'Diana',
            lastName: 'Prince'
        }
    ]
</script>

<!-- {#each names as name(name)}
    <h3>{name.firsName} {name.lastName}</h3>
{/each} -->

{#each names as name(name)}
   <slot name='hero' firstName={name.firstName} lastName={name.lastName}/>
{/each}