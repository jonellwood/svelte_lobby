<script>
  import { onMount } from 'svelte';
  import Holiday from './Holiday.svelte';

  let holidays = [];

  onMount(async () => {
    await fetch (`https://holidayapi.com/v1/holidays?pretty&key=edb48c75-31ef-4c37-94ea-e30a98d9ceeb&country=US&year=2021&month=7`)
    .then(r => r.json())
    .then(data => {
      holidays = data;
    });
    // console.log(holidays.holidays[0].name);
  } )
</script>

{#if holidays.holidays}
  {#each holidays.holidays as holiday }
    <ul class="holiday">
      <li>
        <Holiday {holiday} />
      </li>
    </ul>
  {/each}
{:else}
    <p class="loading">loading...</p>
{/if}

<style>

  .loading {
    opacity: 0;
    animation: 0.4s 0.8s forwards fade-in;
  }
  @keyframes fade-in {
    from { opacity: 0; }
    to { opacity: 1; }
  }
  li {
    list-style-type: none;
  }

</style>
