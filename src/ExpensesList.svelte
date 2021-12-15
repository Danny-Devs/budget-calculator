<script>
  // components
  import SectionTitle from './Title.svelte'
  import Expense from './Expense.svelte'

  // props
  export let expenses = []
</script>

<section>
  <SectionTitle title="expense List" />
  <ul>
    {#each expenses as expense}
      <Expense {...expense} />
    {:else}
      <h2>currently you have no expenses</h2>
    {/each}
  </ul>
</section>

<style>
  h2 {
    text-transform: capitalize;
  }
</style>
